# M6YSM — UK Amateur Radio Tools

A Progressive Web App at [m6ysm.uk](https://m6ysm.uk) for UK amateur radio operators.
DMR talk groups across Brandmeister, TGIF, FreeSTAR and FreeDMR, plus **all UK repeaters**
(FM, DMR, D-Star, Fusion, NXDN, P25, TETRA, Packet) via the RSGB database.

## Features
### Talk Groups
- Live Brandmeister data from the official API
- Curated TGIF, FreeSTAR and FreeDMR UK talk groups
- Search by TG number, name or net info
- Filter by network or "Has net"
- Star favourites (saved to your browser)

### Repeaters
- All UK repeaters from the RSGB ETCC database (official)
- **FM**, **DMR**, D-Star, Fusion, NXDN, P25, TETRA, Packet — all modes
- Enter a UK postcode, town/city, or use your GPS location
- Filter by **15-mile radius** (adjustable 5–50 miles)
- Filter by mode: **All**, **FM only**, or **DMR only**
- Sort by distance, shows frequency, band, CTCSS tone, status

### General
- Offline support via service worker
- Installable on Android (and desktop) as a PWA
- Dark mode support

---

## Files
```
index.html      Main app
sw.js           Service worker (offline caching)
manifest.json   PWA manifest (name, icons, shortcuts)
icon-192.svg    App icon 192×192
icon-512.svg    App icon 512×512
README.md       This file
```

---

## Option 1 — Netlify (easiest, free, 30 seconds)

1. Go to https://netlify.com and sign in (free account)
2. Click **Add new site → Deploy manually**
3. Drag the entire `dmr-talkgroups` folder onto the upload area
4. Done — you'll get a URL like `https://random-name.netlify.app`
5. Optionally set a custom domain in Site settings

---

## Option 2 — GitHub Pages (free, custom domain possible)

1. Create a free account at https://github.com
2. Click **New repository**, name it `dmr-talkgroups`, set to Public
3. Upload all files from this folder to the repo
4. Go to **Settings → Pages → Source → Deploy from branch → main / (root)**
5. Your site will be live at `https://yourusername.github.io/dmr-talkgroups`

---

## Option 3 — Cloudflare Pages (free, fastest CDN)

1. Go to https://pages.cloudflare.com
2. Create a project → **Upload assets**
3. Upload all files from this folder
4. Done — global CDN, custom domain available free

---

## Installing as an Android app

Once the site is live:

1. Open the URL in **Chrome on Android**
2. Tap the **three-dot menu → Add to Home screen**
3. Or tap the **"Install app"** banner that appears in the header
4. The app will appear on your home screen like a native app
5. It works offline once installed

### To create a real APK (optional)
1. Host the site using one of the options above
2. Go to https://pwabuilder.com
3. Enter your URL and click **Start**
4. Download the Android package
5. This gives you a signed APK you can sideload or submit to the Play Store

---

## Running locally (for testing)

You need a local web server — opening index.html directly won't work for
service workers. Quickest options:

```bash
# Python (built in on most systems)
python3 -m http.server 8080
# then open http://localhost:8080

# Node.js
npx serve .
# then open http://localhost:3000
```

---

## Notes

- Brandmeister data is fetched live from api.brandmeister.network on each load
- TGIF, FreeSTAR and FreeDMR data is curated — verify against each network for latest
- Repeater data is fetched from the RSGB Beta API (api-beta.rsgb.online) — the official UK repeater database
- Repeaters are cached in localStorage for offline use
- Favourites are stored in browser localStorage (per device)
- Location geocoding uses OpenStreetMap Nominatim (free, no API key needed)
- Not affiliated with any DMR network or the RSGB

73 de M0XXX
