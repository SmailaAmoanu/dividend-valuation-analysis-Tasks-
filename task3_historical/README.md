# Task 3 — U.S. Valuation, 1825–2025

This task joins the historical NYSE series through 1925 with the Shiller S&P Composite series from 1926 through 2025.

The sources overlap in 1925. Price and dividend levels are aligned separately at that common year before the series are joined. This avoids an artificial jump from the different source scales while preserving historical returns and dividend growth rates.

The missing 1868 low-dividend return in the electronic historical file is set to 4.26%, as reported in the published annual table.

## Files

- `task3_historical.ipynb` — executed notebook
- `task3_historical.html` — rendered report
- `combined_1825_2025.csv` — joined series
- `nyse_data.csv` — historical source data
- `data7.xlsx` — Shiller source data
