# Strava Dark

A self-contained activity tracker built as a single HTML file. Drop in CSV or GPX exports from Garmin, Polar, or Suunto and get an instant dashboard — no account, no server, no install.

![Strava Dark](./strava-dark-preview.png)

---

## Features

- **CSV & GPX support** — works with exports from Garmin, Polar, Suunto, and any standard GPX 1.1 file
- **Auto sport detection** — recognizes skiing, gravel, MTB, hiking, and running from file metadata
- **Activity dashboard** — KPI sidebar, trend charts, monthly volume, sport breakdown, activity heatmap
- **Personal records** — automatically tracks your bests for distance, speed, elevation, duration, HR, and calories
- **Side-by-side compare** — pick any two activities and compare them stat-by-stat with visual bars
- **Season goals** — set targets for distance, elevation, and activity count with live progress bars
- **Dark mode** — full dark theme toggle, persisted across sessions
- **Export** — download all your activities as a clean CSV at any time
- **100% local** — all data lives in your browser's localStorage, nothing is uploaded anywhere

---

## Usage

1. Download `green-mountain-tracker.html`
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge)
3. Drop in your CSV or GPX export files
4. Your dashboard builds instantly

To add more activities later, click **+ Add activities** in the header and drop in new files. Duplicates are skipped automatically.

---

## Supported File Formats

### CSV
Exports from Garmin Connect, Polar Flow, and Suunto app are all supported. The parser recognizes 50+ header name variants including locale differences (e.g. `Distanz (km)`, `Afstand (km)`) and auto-detects comma vs. semicolon delimiters.

### GPX
Standard GPX 1.1 files from any source — Garmin, Strava, Komoot, AllTrails, and more. Distance is calculated via Haversine formula. Heart rate is read from Garmin extensions (`<gpxtpx:hr>`) and standard tags.

---

## Tips

- **Rename the dashboard** — click the title in the header to edit it
- **Filter by sport** — use the tab bar below the header to focus on one activity type
- **Compare activities** — hit ⇄ Compare next to the activity log, pick two activities from the dropdowns
- **Set goals** — edit the number in any goal card to update your season target
- **Escape key** closes any open modal

---

## Privacy

Your data never leaves your device. There are no external API calls, no analytics, no tracking. The only network requests are loading fonts from Google Fonts and the Chart.js library from a CDN on first open — everything else runs offline.

---

## Tech

Single HTML file (~270KB including embedded logo). Vanilla JS, no frameworks. Chart.js for visualizations. Barlow / Barlow Condensed for typography.
