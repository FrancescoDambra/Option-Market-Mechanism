# SX5E Options Market Mechanics Simulator

A Python simulation of institutional options market dynamics built on the **Euro Stoxx 50 (SX5E)** index. This project models the mechanical forces that drive real intraday equity moves — dealer gamma hedging, vanna flows, implied volatility surface dynamics, and net gamma exposure.

---

## Concepts Covered

| Concept | Description |
|---|---|
| **Black-Scholes Pricing** | European call and put pricing with full Greek derivation |
| **Volatility Skew** | Realistic equity skew model — OTM puts trade at higher IV than OTM calls |
| **3D IV Surface** | Full implied volatility surface across strikes and expiries |
| **Delta & Gamma** | Dealer hedge ratios and rehedging cost per unit move |
| **Vanna** | Delta sensitivity to IV — the driver of mechanical rallies and selloffs |
| **Net Gamma Exposure (GEX)** | Aggregate dealer gamma by strike — positive vs negative regimes |
| **Vanna Flow Analysis** | Simulated dealer flows under IV stress and relief scenarios |
| **Full Scenario Simulation** | Complete intraday path simulation from calm to crisis to recovery |

---

## Notebook Structure

The notebook is organized into 8 sequential cells:

**Cell 1 — Imports and Parameters**
Libraries and SX5E market parameters (spot, rate, strikes, expiries).

**Cell 2 — Black-Scholes Engine**
Pricing function returning call price, put price, delta, gamma, and vanna for any input set.

**Cell 3 — Volatility Skew**
Strike-dependent IV function replicating the structural equity skew.

**Cell 4 — 3D Implied Volatility Surface**
High-resolution 3D surface plot across 50 strikes and 50 expiry tenors.

**Cell 5 — Dealer Book**
Full option chain simulation: 9 strikes × 4 expiries with realistic open interest and dollar gamma.

**Cell 6 — GEX Chart**
Aggregate net gamma exposure by strike — the dealer hedging map.

**Cell 7 — Vanna Flow Analysis**
Side-by-side dealer flow charts under IV +5% stress and IV -5% relief scenarios.

**Cell 8 — Full Scenario Simulation**
Complete intraday simulation: spot path, IV path, and GEX map on a single chart.

---

## Key Outputs

**3D Implied Volatility Surface**
A smooth, high-resolution surface showing the volatility skew across all strikes and expiries. The left side (OTM puts) is always higher than the right side (OTM calls) — reflecting structural institutional demand for downside protection.

**GEX Chart**
A bar chart showing dollar gamma by strike. The tallest bars indicate where dealer hedging flows are most concentrated — and where gamma pinning occurs near expiry.

**Vanna Flow Charts**
Two side-by-side charts showing the direction and magnitude of mechanical dealer flows under an IV shock. Crimson bars mean dealers must sell. Green bars mean dealers must buy.

**Full Scenario Simulation**
Three stacked charts — spot price, IV path, and GEX map — telling the complete story of a stress event from open to close.

---

## Author

**Francesco Dambra**
MSc Banking and Finance — Università Cattolica del Sacro Cuore, Milan
