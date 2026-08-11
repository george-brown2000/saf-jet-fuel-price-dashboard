# SAF / Jet Fuel Market Monitor

An interactive market intelligence dashboard tracking the economics of sustainable aviation fuel (SAF) relative to fossil jet fuel, built as a portfolio piece demonstrating sector expertise and quantitative analytical capability.

**[Live dashboard →](https://george-brown2000.github.io/saf-market-dashboard)**

---

## What this dashboard does

The dashboard answers the core question a commodities trader, project finance analyst, or energy equity researcher asks about SAF: **what does it cost relative to fossil jet, what closes the gap, and is the economics improving?**

Four analytical panels:

| Panel | What it shows |
|---|---|
| **Price history** | Jet A-1 CIF NWE vs. HEFA-SAF price, SAF premium over time, and UK ETS carbon price overlay (2019–2025) |
| **Cost structure** | Waterfall decomposition of the $1,200/t SAF premium — feedstock, conversion CAPEX/OPEX, logistics, RTFO certificate income, and residual gap |
| **UK mandate** | RTFO SAF blending obligation trajectory to 2030, statutory target vs. estimated compliance, and implied volume demand |
| **Scenarios to 2030** | Interactive scenario model — toggle carbon price path (low/base/high) and mandate enforcement (weak/base/strong) to project SAF premium trajectory |

---

## Data sources

| Series | Source |
|---|---|
| Jet A-1 spot price | US EIA kerosene-type jet fuel price (converted to $/t) |
| HEFA-SAF price | Indicative, calibrated to Argus Media, ICIS, IATA, and NREL published benchmarks |
| SAF premium | Derived: SAF minus Jet A-1 |
| UK ETS carbon price | ICE auction results and secondary market data |
| RTFO mandate trajectory | UK DfT RTFO statistics and SAF mandate statutory instruments (RTFO SAF Order 2024) |
| Scenario projections | Model-based estimates using documented assumptions — not forecasts |

> **Note on data:** HEFA-SAF spot price data is largely paywalled (Argus, ICIS, OPIS). The prices used here are indicative figures calibrated to published sources and academic literature. Wiring to a live data feed (EIA API, Ember, or an Argus subscription) is a planned enhancement — see roadmap below.

---

## Why SAF and why now

SAF is one of the most capital-intensive and policy-sensitive decarbonisation plays in aviation. The economics are driven by three interacting forces:

1. **Feedstock cost** — UCO (used cooking oil) and tallow dominate current HEFA supply; prices are volatile and linked to global vegetable oil markets
2. **Mandate-driven demand** — the UK RTFO trajectory to 10% by 2030 (22% by 2040) creates a policy floor for demand; enforcement quality determines actual volume
3. **Carbon pricing** — UK ETS covers aviation; a rising carbon price structurally narrows the SAF premium by increasing the cost of fossil jet to operators

Understanding how these three interact is the core analytical challenge for anyone pricing SAF offtake agreements, modelling project IRRs, or taking a view on feedstock commodity markets.

---

## Technical

- Pure HTML/CSS/JS — no build step, no dependencies beyond Chart.js (CDN)
- Single `index.html` file — deployable anywhere static files are served
- Fully responsive

### Run locally

```bash
git clone https://github.com/george-brown2000/saf-market-dashboard.git
cd saf-market-dashboard
open index.html   # or serve with any static file server
```

### Deploy to GitHub Pages

1. Push `index.html` to the `main` branch of your repository
2. Go to **Settings → Pages → Source → main / root**
3. GitHub Pages will publish it at `https://<username>.github.io/<repo-name>`

---

## Roadmap

- [ ] Wire EIA API for live Jet A-1 price data
- [ ] Add UCO / tallow feedstock price series (FAO/USDA proxy)
- [ ] EU ETS vs. UK ETS spread panel
- [ ] Feedstock price sensitivity toggle in scenario model
- [ ] RefuelEU mandate overlay alongside UK RTFO (EU comparison)
- [ ] Downloadable scenario output as CSV

---

## About

Built by **George Brown** — process engineer with experience across CCUS, sustainable aviation fuel (Alcohol-to-Jet pathway), and LNG at Technip Energies and Anthesis. MEng Chemical Engineering, University of Nottingham (First Class Honours).

This dashboard is part of a broader portfolio demonstrating the intersection of technical sector knowledge and financial/commercial analysis in energy markets.

[LinkedIn](https://linkedin.com/in/george-brown2000) · [GitHub](https://github.com/george-brown2000)
