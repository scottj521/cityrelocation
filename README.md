# 🏠 City Relocator — Neighborhood Research Hub

A static, AI-powered neighborhood research tool for finding the best counties and cities to live in across the United States. Built for a **teacher + remote worker dual-income household** context.

## Features

- **County & city-level QOL grades** (A+ through D) with real data
- **Racial demographic pie charts** per city (US Census ACS 2020–2024)
- **Rent, home prices, crime, schools** breakdowns for every city
- **AI-powered "Add State"** — generates a full county/city breakdown for any US state on demand
- **AI-powered "Add City"** — adds any city to an existing state page with full stats + demographics
- **Cross-comparison table** for every state
- **GitHub Pages ready** — fully static, no server required

## States Included

| State | Counties | Cities | Status |
|-------|----------|--------|--------|
| Georgia | 6 | 9 | ✅ Live |
| South Carolina | 5 | 11 | ✅ Live |
| Any US State | AI-generated | AI-generated | ✦ On Demand |

## How to Use Locally

Just open `index.html` in a browser. No build step, no server, no dependencies.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/city-relocator.git
cd city-relocator

# Open in browser (Mac)
open index.html

# Open in browser (Windows)
start index.html
```

## Deploy to GitHub Pages

1. Push to GitHub
2. Go to **Settings → Pages**
3. Set Source to `main` branch, `/ (root)` folder
4. Your hub will be live at `https://YOUR_USERNAME.github.io/city-relocator/`

## AI Features (Anthropic API)

The "Add State" and "Add City" buttons call the Anthropic Claude API directly from the browser. This works out of the box — no API key required on your end (uses Anthropic's browser-accessible endpoint via claude.ai artifact context).

> **Note:** AI-generated state pages and added cities are stored in memory for the current session only. Refresh resets them. To persist a generated state, copy the rendered HTML and save it as a new `.html` file in this repo.

## File Structure

```
city-relocator/
├── index.html          # Hub landing page (start here)
├── georgia.html        # Georgia — full county + city breakdown
├── south-carolina.html # South Carolina — full county + city breakdown
├── shared.css          # Shared styles (imported by all pages)
└── README.md
```

## Data Sources

- [Niche](https://niche.com) — County & city grades
- [AreaVibes](https://areavibes.com) — Livability scores
- [SafeWise](https://safewise.com) — Crime rankings
- [HUD Fair Market Rents](https://huduser.gov) — 2025–2026 FMR data
- [Redfin](https://redfin.com) / [Zillow](https://zillow.com) — Home prices
- [FBI UCR](https://ucr.fbi.gov) — Violent crime statistics
- [US Census Bureau ACS](https://census.gov) — Demographics (2020–2024 5-Year Estimates)

## Contributing

This is a personal research tool. Feel free to fork and add your own states.
