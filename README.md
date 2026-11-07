# Tideline

Tideline ranks San Diego beaches for a swim. Drop a pin, pick a day and time, and it ranks every beach nearby by water quality, swim safety, water comfort, crowds, weather and drive time.

**Live site:** `https://jahemas22.github.io/MIH-Hackathon/` (after GitHub Pages is turned on)

## How the score works

Score = 100 × G × Q

- **G (water quality, 0–1):** County status × rain runoff × Tijuana River sewage factor. Because it multiplies everything, bad water can never be outweighed.
- **Q (conditions, 0–1):** swim safety (35%), water comfort (25%), crowds (20%), weather (12%) and drive time (8%), blended 60% geometric mean and 40% weighted average. Users can change the weights with sliders.

## Data sources

| Data | Source | Status |
|---|---|---|
| Weather (temperature, sky, wind, rain chance) | National Weather Service hourly forecast | Live |
| Tides | NOAA Tides & Currents (La Jolla and San Diego Bay stations) | Live |
| Water temperature | NOAA Tides & Currents | Live |
| Restaurants | OpenStreetMap (Overpass API) | Live |
| Beach photos | Wikipedia / Wikimedia Commons | Live |
| Map | Leaflet with OpenStreetMap / Esri tiles | Live |
| Crowds | Historical attendance model (month, weekday, hour, weather, events) | Model |
| Water quality | County of San Diego, sdbeachinfo.com | Updated by hand |
| Waves, rip current risk, bus fullness | Example values | Demo |

## Updating water quality by hand

The County has no public data feed. Before a demo, check https://www.sdbeachinfo.com and edit the `quality` value for each beach in the `BEACHES` list in `index.html` (`"good"`, `"advisory"` or `"closed"`). Recent rain goes in the `RAIN` setting.

## Running it

It's a single file. Open `index.html` in a browser, or host it on GitHub Pages. No API keys needed.
