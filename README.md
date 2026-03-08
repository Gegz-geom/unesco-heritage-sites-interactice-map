# 🏛 UNESCO World Heritage Sites Explorer

An interactive web map explorer of 120 UNESCO World Heritage Sites built with Leaflet.js. Features filtering by type, continent, country and year, real-time dashboard stats, 3 switchable basemaps, and a fully responsive mobile-first design with a slide-up bottom sheet.

🌍 **Live Demo:** [https://gegz-geom.github.io/unesco-heritage-sites-interactice-map/](https://gegz-geom.github.io/unesco-heritage-sites-interactice-map/)

---

## Features

- 120 UNESCO World Heritage Sites across 6 continents
- Filter by **type** (Cultural, Natural, Mixed), **continent**, **country**, and **inscription year**
- **In Danger** toggle to highlight at-risk sites
- Real-time **dashboard** showing site counts and type breakdown
- **3 basemaps** — Dark, Satellite, and Terrain
- Popup cards with site description, region, category, and status
- **Fully responsive** — mobile bottom sheet with collapsible filters and searchable site list
- Zero external API calls — all data is embedded

---

## Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 / CSS3 | Structure & styling |
| JavaScript (ES6+) | App logic & interactivity |
| [Leaflet.js v1.9.4](https://leafletjs.com/) | Interactive map rendering |
| CartoDB Dark Matter | Default basemap tiles |
| ESRI World Imagery | Satellite basemap tiles |
| OpenTopoMap | Terrain basemap tiles |
| Google Fonts | Playfair Display + DM Sans |

---

## Data

The dataset of 120 sites was curated from UNESCO World Heritage records and embedded directly as a static JavaScript array. Each site includes:

```js
{
  id, name, country, continent,
  type,       // "Cultural" | "Natural" | "Mixed"
  lat, lng,   // coordinates
  year,       // inscription year
  danger,     // boolean — on UNESCO Danger List
  desc        // short description
}
```

> To extend with the full 1,200+ sites, use the official [UNESCO API](https://whc.unesco.org/en/syndication).

---

## Project Structure

```
unesco-heritage-map/
├── index.html       # Main application (single-file)
├── favicon.svg      # Site favicon
├── README.md        # Project documentation
└── LICENSE          # MIT License
```

---

## Getting Started

No build tools or dependencies needed. Just open `index.html` in a browser, or serve it with any static file server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (npx)
npx serve .
```

---

## Screenshots

> Map loads with 120 sites plotted across a dark basemap. Sidebar shows filters, dashboard stats, and a scrollable site list. Clicking a marker opens a popup with site details.

---

## License

MIT — free to use and adapt with attribution.
