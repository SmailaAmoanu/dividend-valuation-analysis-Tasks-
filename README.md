# Dividend-Based Valuation Analysis

This repository contains Tasks 0–4 of the dividend-based valuation analysis. Each task is kept in a separate directory with its source data, executed notebook, rendered HTML report, and a short README.

## Tasks

| Task | Sample | Analysis |
|---|---|---|
| Task 0 | International market and developed countries | International and country-level valuation |
| Task 1 | 1871–2025 | Shiller S&P Composite valuation |
| Task 2 | Historical fit through 2000; prediction 2021–2025 | Out-of-sample prediction |
| Task 3 | 1825–2025 | Long U.S. historical valuation |
| Task 4 | 1926–1957 | Early S&P subperiod analysis |

## Selected results

| Task | \(b\) | \(c\) | 95% interval for \(c\) | ADF p-value |
|---|---:|---:|---:|---:|
| Task 1 | 0.8614 | 5.09% | 4.64%–5.48% | 0.0117 |
| Task 2 | 0.7410 | 5.71% | 4.77%–7.11% | 0.0158 |
| Task 3 | 0.7665 | 5.39% | 5.16%–5.63% | 0.0080 |
| Task 4 | 0.6629 | 5.51% | 2.72%–10.13% | 0.0496 |

Task 0 contains the international aggregate and country-level comparison table in its own notebook and `country_summary.csv`.

## Common model

For price level \(S_t\) and dividend \(D_t\),

$$
Q_t=\log(S_t+D_t)-\log(S_{t-1}),
$$

$$
G_t=\log(D_t)-\log(D_{t-1}).
$$

With \(C_t\) denoting the cumulative sum of \(Q_t-G_t\),

$$
Q_t-G_t=\alpha+\beta t-\gamma C_{t-1}+Z_t.
$$

The equivalent parameterization is

$$
b=1-\gamma,\qquad
c=\frac{\beta}{\gamma},\qquad
a=\alpha-bc,
$$

and

$$
H_t=C_t-ct.
$$

## Repository structure

```text
task0_international/
task1_shiller/
task2_prediction/
task3_historical/
task4_1926_1957/
```

The notebooks contain the data construction, parameter estimates, confidence intervals, valuation plots, mean-reversion checks, and residual diagnostics. Task 2 additionally contains the 2021–2025 out-of-sample comparison.


## Notebook style

All notebooks use the same reporting structure: data loading, valuation-variable construction, model estimation, valuation plots, confidence intervals, and residual diagnostics. Code is divided into short analytical steps rather than large all-in-one cells.
