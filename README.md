# Krish's Portfolio

An interactive **macOS Sonoma-style desktop**, built as a single HTML file with no framework.

**→ [krish57-bit.github.io](https://krish57-bit.github.io/)**

Instead of scrolling a landing page, you get a desktop that boots up in your browser: a systemd-style startup log, translucent windows with real traffic-light buttons, a Dock, live weather in the menu bar, an interactive Terminal REPL, ⌘K Spotlight, a Finder-style project grid, and a playable Minesweeper.

---

## Features

- **systemd-style boot log** — real service names (FastAPI on `:8000`, Kafka broker, Redis on `:6379`, MongoDB replica set…) stream with millisecond timings before the desktop appears.
- **Interactive Terminal (Skills window)** — real REPL, not just a typed animation. Try `help`, `whoami`, `open projects`, `cat about`, `github`, `sudo hire me`. `↑ / ↓` walks history, `Ctrl+L` clears.
- **Spotlight** (`⌘K` / `Ctrl+K`) — fuzzy search across projects, sections, and links.
- **Live weather in the menu bar** — IP-geolocated (no permission prompt), Open-Meteo API, click for the 3-day forecast.
- **Live GitHub activity in the menu bar** — "3h ago" tag pulled from the GitHub public events API.
- **Minesweeper** — classic 9×9, 10 mines. First click always safe, timer, flag counter, click the face to restart. Living inside a proper window (drag, close, minimize, zoom).
- **Draggable + zoomable + closable windows** — every traffic-light button does what it says: red closes, yellow hides, green zooms/restores.
- **Menu bar app menus** — File · Edit · View · Window · Games · Help with real actions (Copy Email, Open Resume, Reboot krishOS, dynamic Window list, View Source, Report an Issue).
- **Finder-style Projects view** — each project links to its own GitHub repo.
- **Contact form** with mailto composition + copy-to-clipboard fallback.
- **Accessibility** — respects `prefers-reduced-motion`: skips wallpaper drift, boot animation, and terminal typing.
- **Share-ready** — Open Graph + Twitter meta tags, custom SVG favicon.

## Tech

- **Vanilla HTML / CSS / JS** — no framework, no build step, no npm install.
- **~2000 lines** in a single `index.html` (~100 KB).
- **Google Fonts**: Inter (UI), JetBrains Mono (terminal + code).
- **External APIs**:
  - [Open-Meteo](https://open-meteo.com/) — current + 3-day forecast, no key.
  - [ipapi.co](https://ipapi.co/) — coarse IP geolocation for the weather widget.
  - [GitHub REST](https://docs.github.com/rest/activity/events) — public events for the activity indicator.
- Deployed on **GitHub Pages**.

## Run locally

Just open `index.html` in a browser. Or if you want a proper origin (needed for a couple of the fetches):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## About me

I'm **Krish Kaul** — final-year Electronics & Computer Engineering student at Thapar Institute, Patiala. Backend & distributed-systems focus.

Recent work you'll find inside the portfolio:

- **Kavach AI** — real-time industrial-risk monitoring · ET AI Hackathon 2026
- **SBI FlowSense** — event-driven banking workflow · SBI Hackathon @ Global Fintech Fest 2026
- **MATDATA** — matrimonial-data assistant · Google AI Hackathon (Cloud Run in 48h)
- **Wanderlust** — full-stack travel platform
- **PARAKH** — capstone research, IIT Ropar incubation review (team lead)

**Contact**: [GitHub](https://github.com/krish57-bit) · [LinkedIn](https://www.linkedin.com/in/krish-kaul-0b6bb3233/) · [LeetCode](https://leetcode.com/u/krish_231/) · krishkaul57@gmail.com

## License

MIT — see [`LICENSE`](./LICENSE). Fork it, but please write your own copy — the point of a portfolio is that it's yours.
