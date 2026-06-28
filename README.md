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




