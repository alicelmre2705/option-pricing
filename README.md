# Derivatives Pricing Lab — Hedging & Risk

Monte Carlo option pricing engine validated against Black-Scholes, with delta hedging proof, Greeks P&L attribution, barrier options with BGK correction, and volatility smile from fat tails.

## Results

| Metric | Value |
|--------|-------|
| MC vs BS error | < 0.03 |
| BGK bias reduction | $0.23 → $0.05 |
| Greeks P&L explained | 100.1% |
| Daily hedging residual | 5.7% of C₀ |
| Student-t(5) kurtosis | 8.4 (vs 3.0 normal) |

## Structure

- `derivatives_pricing_lab_EN.ipynb` — Full implementation with explanations
- `Monte_Carlo_Option_Pricing_Report.pdf` — Academic report (6 pages, LaTeX)

## What's covered

1. **European option pricing** — 200k-path MC engine, validated against BS closed-form
2. **Barrier options** — Down-and-out call pricing across barrier levels, path simulation
3. **BGK correction** — Fixes discrete-monitoring bias on barrier contracts
4. **Delta hedging** — 50k simulations prove BS price = replication cost (mean P&L ≈ 0 regardless of drift μ)
5. **Greeks & P&L attribution** — Analytical Delta, Gamma, Vega, Theta; Taylor decomposition of daily P&L
6. **Volatility smile** — Student-t returns generate the smile observed in real markets

## Requirements

```
numpy
matplotlib
scipy
```

## Author

Alice Lemaire — alice.lemaire.pro@outlook.com
