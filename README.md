# CAPM and Fama-French 3-Factor Analysis — Euronext 100

## Overview

This project conducts **CAPM** and **Fama-French 3-Factor regression analysis** on five stocks from the Euronext 100 index. The goal is to decompose each stock's returns and identify exposure to systematic risk factors: market risk, size (SMB), and value (HML).

All data is retrieved automatically from Yahoo Finance and the Kenneth French Data Library using Python.

---

## Stocks Analysed

| Ticker | Company | Sector |
|--------|---------|--------|
| INGA.AS | ING Groep N.V. | Banking |
| KER.PA | Kering SA | Luxury Goods |
| HO.PA | Thales S.A. | Defence & Aerospace |
| GALP.LS | Galp Energia | Energy |
| IPN.PA | Ipsen S.A. | Pharmaceuticals |

**Index Benchmark:** Euronext 100 (`^N100`)
**Analysis Period:** November 2020 – November 2025 (5 years)
**Risk-Free Rate:** 3% (annualised)

---

## What This Project Does

For each of the five stocks:

1. Downloads 5 years of historical adjusted closing prices from Yahoo Finance.
2. Plots price history vs. the Euronext 100 index.
3. Runs **OLS regression for CAPM** (market risk premium vs. asset excess returns).
4. Plots the regression scatter with fitted line.
5. Runs **Fama-French 3-Factor OLS regression** using factors from the Kenneth French Data Library.
6. Interprets each model's output: R², Beta, Alpha, SMB/HML exposure, and p-values.

---

## Models Used

### CAPM
$$E(R_i) = R_f + \beta_i(E(R_m) - R_f)$$

- Estimates systematic market exposure (Beta).
- Identifies whether the stock is more or less volatile than the market.

### Fama-French 3-Factor Model
$$R_{i,t} - R_{f,t} = \alpha_i + \beta_{i,M}(R_{M,t} - R_{f,t}) + \beta_{i,SMB}SMB_t + \beta_{i,HML}HML_t + \epsilon_{i,t}$$

- **Mkt-RF:** Market risk premium
- **SMB (Small Minus Big):** Size factor
- **HML (High Minus Low):** Value factor

---

## Tech Stack

```
Python 3 | yfinance | pandas | matplotlib | scipy | statsmodels | seaborn | pandas_datareader
```

---

## Project Structure

```
capm-fama-french-euronext/
│
├── capm_fama_french_euronext100.ipynb   # Full analysis notebook (all 5 stocks)
└── README.md
```

---

## Installation

```bash
pip install yfinance matplotlib pandas scipy pandas_datareader seaborn statsmodels
```

---

## Concepts Demonstrated

- **Ordinary Least Squares (OLS) regression** for financial modelling
- **CAPM** for single-factor risk decomposition
- **Fama-French 3-Factor Model** for multi-factor asset pricing
- **Jensen's Alpha** — measuring risk-adjusted outperformance
- **Beta interpretation** — systematic vs. idiosyncratic risk

---

## Author

**Mohammad Osama Khan**
MSc Financial Economics — Otto-von-Guericke University Magdeburg
[LinkedIn](https://www.linkedin.com/in/mohammad-osama-khan-93233a191) | mohammad2.khan@st.ovgu.de
