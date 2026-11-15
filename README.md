# 🌱 AgroPulse: NASA-Driven Crop Rotation Intelligence

NASA Space Apps Challenge · Team **MMSS** (Mohammad Soliman) · Challenge: Agriculture & Crop Rotation

AgroPulse is a single-page, bilingual (EN/AR) decision-support web app that recommends the next crop in a rotation using NASA climate and soil-wetness data plus transparent agronomic rules.

## Run
Open `index.html` in a browser, or publish with **GitHub Pages** (Settings → Pages → Deploy from branch → `main` / root).

## How it works
1. User picks a location (or enters lat/lon), soil type, previous crop, and irrigation availability.
2. The app calls the **NASA POWER API** (no key needed) for the last 3 full years: precipitation (`PRECTOTCORR`, GPM/IMERG-based), temperature (`T2M`), root-zone wetness (`GWETROOT`, MERRA-2).
3. A **transparent rule-based scoring model** ranks 9 crops (0–100) and shows the reason behind every point: plant-family change (pest/disease cycle), nitrogen balance (legumes), water need vs supply, temperature range, soil suitability.
4. If NASA POWER is unreachable, approximate built-in demo values are used and clearly labeled.

## NASA data
- NASA POWER (Prediction Of Worldwide Energy Resources), agroclimatology community
- GPM IMERG-based precipitation; MERRA-2 meteorology and soil wetness

## Limitations (honesty note)
Rule-based, not machine learning. Crop parameters are simplified agronomic values; validate with local extension services. Future work: SMAP soil-moisture layers, trained models on regional yield data.

---

## Hackathon form text (accurate version)

**Project Name:** AgroPulse: NASA-Driven Crop Rotation Intelligence

**High-Level Summary:** AgroPulse is an interactive web tool that helps farmers choose the next crop in their rotation. It combines NASA climate and soil-wetness data with transparent agronomic rules to improve soil health, save water, and build resilience to climate change.

**Use of AI:** We use an explainable rule-based scoring model (no black box) that ranks crops and states the reason for each recommendation. Machine learning on regional yield data is planned future work.

**NASA Data:** NASA POWER API (GPM/IMERG-based precipitation, MERRA-2 temperature and root-zone soil wetness). SMAP is planned as a future layer.

**Other References:** Standard crop-rotation agronomy (plant-family rotation, legume nitrogen fixation) and local extension guidelines.

---

## 7-slide presentation

1. **Title:** AgroPulse, Team MMSS, tagline, logo.
2. **Problem:** Climate change and soil degradation make rotation planning hard; wrong sequences spread pests and drain nutrients.
3. **Solution:** A smart digital agronomist: location + soil + last crop → ranked next crops.
4. **NASA data:** POWER (GPM precipitation, MERRA-2 temperature and soil wetness), with a diagram of data → scoring → advice.
5. **Live demo:** Screenshot of the top-3 results with the reasons list.
6. **Impact:** Healthier soil, less water waste, fewer pest outbreaks, bilingual access for farmers.
7. **Roadmap and team:** SMAP layers, ML on yield data, mobile/SMS access; team members and links.

## 30-second video script
- 0–5s: "Farmers worldwide face drought, heat and tired soil."
- 5–12s: "We're Team MMSS, and this is AgroPulse."
- 12–22s: Screen recording: choose location, soil, last crop → live NASA data → top-3 crops with reasons.
- 22–30s: "Powered by NASA POWER data, AgroPulse turns satellite data into rotation decisions. Healthier soil, smarter water."

## Repo structure
```
agropulse/
├── index.html
├── README.md
└── LICENSE   (add MIT via GitHub: Add file → Create new file → LICENSE)
```
