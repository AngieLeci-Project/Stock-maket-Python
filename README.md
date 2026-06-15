# Indonesia Blue-Chip Stock Market Analysis — Python

Exploratory data analysis on 4 Indonesian blue-chip stocks using Python.

---

## Overview

This project performs EDA on historical price data from 4 major Indonesian blue-chip stocks listed on the Indonesia Stock Exchange (IDX). Using 21,425 trading records spanning **2001–2023**, the analysis computes key financial metrics and visualizes price trends, volatility, and cumulative returns across all four stocks.

---

## Stocks Analyzed

| Ticker | Company | Records |
|--------|---------|---------|
| BBCA | Bank Central Asia | 5,670 |
| BBNI | Bank Negara Indonesia | 5,670 |
| BMRI | Bank Mandiri | 5,085 |
| BBRI | Bank Rakyat Indonesia | 5,000 |

---

## Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python |
| Data Processing | pandas, NumPy |
| Visualization | matplotlib, seaborn |
| Environment | Jupyter Notebook |

---

## Dataset

- **Source:** BBCA.csv, BBNI.csv, BBRI.csv, BMRI.csv
- **Period:** 2001–2023

---

## Workflow

```
1. Data Loading
   - Loaded 4 CSV files and merged into single DataFrame
   - Added Stock ticker column for multi-stock analysis
        ↓
2. Data Cleaning & Validation
   - Converted timestamp to datetime
   - Sorted by Stock and date
   - Verified no missing values
        ↓
3. Feature Engineering
   - Daily Return (pct_change)
   - MA_20 & MA_200 (rolling moving averages)
   - Volatility (20-day rolling std of returns)
   - Cumulative Return
        ↓
4. Visualization
   - Stock price trend (all 4 stocks)
   - Return distribution (KDE plot)
   - Moving average chart (MA20 vs MA200)
   - Volatility over time
   - Cumulative returns comparison
```

---

## Key Findings

- BBCA showed the strongest cumulative return over the 2001–2023 period
- All 4 stocks exhibit similar volatility patterns, spiking during market downturns
- MA20/MA200 crossovers visible during major bull and bear cycles
