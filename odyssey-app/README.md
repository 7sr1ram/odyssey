# Odyssey — Southampton walking-route comparison

**Run it:** `python3 -m http.server 8000` in this folder, then open
http://localhost:8000. No backend, no accounts, no keys.

- **Map:** mapped walking segments are coloured by Athena's model band
  (green lower / amber medium / red higher / grey-dashed = no lighting data).
  Click a segment for its historical data, mapped street attributes and sources.
- **Routing:** Shortest / Model-preferred / Balanced. The model-preferred route
  weighs Athena's scores more heavily, with a 12-minute detour bound. If two
  profiles lead to the same path, both are shown and labelled honestly.
- **Live:** the panel fetches the real-time Environment Agency tide gauge at
  Woolston and active flood warnings directly in your browser.
- **Handoff:** Google Maps receives the start and destination only and may
  calculate a different walking path from the one shown here.
- **SOS:** 999 / 101 dial buttons, copy-my-location, official guidance links.
- **Honesty:** `node test_core.js` verifies routes on the real data;
  `data/data_manifest.json` lists every source with its licence and fetch
  date; `data/model.json` is the full model card (AUC 0.971 vs 0.866
  recency baseline on held-out Aug 2026). Model bands do not guarantee
  personal safety. The app does not submit route feedback to a server.

Regenerate all data + retrain the model: see `../odyssey-city-data`.
Full write-up and demo script: `../GUIDE.md` and `../odyssey-city-data/README.md`.

Licences: OSM ODbL (basemap, network) · Police UK & EA OGL v3 · Leaflet BSD · code MIT.
