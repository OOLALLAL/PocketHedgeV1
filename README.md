# Pocket Hedge v1 – Portfolio Risk Analyzer (JavaScript)

Pocket Hedge v1 is a lightweight, client-side portfolio analysis tool built with JavaScript and jQuery.  
It provides quick risk metrics for a user-defined equity portfolio using daily price data from Stooq.

This version focuses on clean implementation and transparent calculations without external backend services.


## Features
- Fetches daily OHLC data directly from Stooq (client-side)
- Supports custom portfolios and weight inputs
- Computes key risk metrics:
  - Log returns
  - Portfolio beta vs benchmark (QQQ/SPY/DIA)
  - Correlation
  - Daily & annualized volatility
  - Historical VaR (95%)
- Local caching for benchmark data to reduce network calls
- Simple, responsive UI for fast interaction


## Tech Stack
- HTML, CSS
- JavaScript (ES6)
- jQuery  
- Stooq CSV endpoints


## How It Works
1. User enters symbols and weights (must total 100%).
2. The app loads benchmark data (cached for 24 hours).
3. For each symbol, daily close prices are fetched from Stooq.
4. Log returns are computed and aligned by date.
5. Risk metrics are calculated on the overlapping time window.
6. Results are displayed in JSON format.

No server, no build tools — everything runs in the browser.


## Notes
- This is the first iteration of Pocket Hedge (v1).  
- Pocket Hedge v2 (Python) expands this into automated hedge-pair discovery and performance-based recommendations.


## License
MIT
