# Orbit Calendar

A free, offline-first calendar and appointment PWA. No accounts, no paid APIs, no build step.

## Run it
1. Host the files over HTTPS (e.g. GitHub Pages) or run `python -m http.server` here and open `http://localhost:8000`.
2. Use your browser's **Install** option to add it as an app.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML, CSS, JS) |
| `manifest.webmanifest` | Install metadata |
| `sw.js` | Service worker: offline caching (same-origin only) |
| `icon.svg`, `icon-192.png`, `icon-512.png` | App icons |

## Your data
- Stored in IndexedDB; the app requests persistent storage.
- **Menu → Auto-backup to a file** (Chromium browsers) mirrors every change to a file you choose, so data survives a browser reset. Restore with **Import JSON backup**.
- JSON and `.ics` import/export are in the menu.

## Features
- Month, week, day and agenda views; mini-calendar; search; 6 colour themes (Menu) each with a matching dark mode; print
- Repeats (every N days/weeks/months/years), all-day events, per-event colours, drag-and-drop, side-by-side overlaps
- Quick add: `Dentist tomorrow 3pm for 45m`, `Standup every week 9:30am`, `note: buy milk`
- Notes: general, day-attached or time-slot-attached (Alt+double-click a day or slot)
- Reminders with travel time ("leave by"), conflict warnings, undo delete, edit or delete one occurrence
- Find free time, copy availability as text
- Weather (Open-Meteo, optional): Menu → Enable weather, or tap the 🌤 chip under the toolbar (falls back to entering your city if location is blocked). Location is rounded and kept on-device. Each day's weather is recorded and kept after the day passes; future days are forecasts and update.

## Shortcuts
`N` quick add · `M/W/D/A` views · `T` today · `←/→` navigate

## Known limits
No server, so no booking links or multi-user sharing.
