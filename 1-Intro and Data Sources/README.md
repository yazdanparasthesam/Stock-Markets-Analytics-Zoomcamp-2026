# 📋 Module 1 Homework Answers (2026 cohort)
*Stock Markets Analytics Zoomcamp — Module 01: Introduction and Data Sources*

---

## Question 1 — S&P 500 Additions

| Item | Answer |
|---|---|
| **Year with most additions since 2020** | **2025** (18 additions) |
| Additions breakdown (2020→2026) | 2020=10, 2021=10, 2022=15, 2023=15, 2024=16, **2025=18**, 2026=13 (partial year, excluded) |
| **Additional:** Stocks in index > 20 years | **~224** (added before 2006-09-14); if "added ≤ 2005" → **218** |

> ✅ **Pick: 2025** (and ~224 for the additional, if asked)

---

## Question 2 — World Indices YTD (as of 21 Aug 2026)

| Index | YTD return | Beats S&P 500? |
|---|---|---|
| Japan - Nikkei 225 | **+27.36%** | ✅ |
| Canada - S&P/TSX Composite | **+14.86%** | ✅ |
| **United States - S&P 500** | **+11.90%** | (benchmark) |
| UK - FTSE 100 | +8.70% | ❌ |
| Brazil - Ibovespa | +6.54% | ❌ |
| Germany - DAX | +6.51% | ❌ |
| Australia - S&P/ASX 200 | +3.79% | ❌ |
| Mexico - IPC Mexico | +2.48% | ❌ |
| Hong Kong - Hang Seng | −1.25% | ❌ |
| China - Shanghai Composite | −2.94% | ❌ |
| India - Nifty 50 | −7.25% | ❌ |

> ✅ **Pick: 2 indices beat S&P 500 YTD (Japan + Canada)**

**Additional (3y / 5y / 10y):** Same trend — only Japan & Canada beat US over 3y (2) and 5y (2); over 10y only Japan (1). The US remains the global leader over the long run.

---

## Question 3 — S&P 500 Corrections (≥5%) since 1950

**74 significant corrections identified.** Top-10 drawdowns match the homework hint exactly ✓.

| Statistic | Drawdown % | Duration (ATH→trough, days) | Recovery (ATH→new ATH, days) |
|---|---|---|---|
| 25th percentile | 6.23% | 22 | 56 |
| **50th (median)** | **≈ 8% (7.99%)** | **40** | **92** |
| 75th percentile | 14.02% | 86 | 212 |

**Top 10 largest corrections (verification against hint):**

| Period | Drawdown | Duration |
|---|---|---|
| 2007-10-09 → 2009-03-09 | 56.8% | 517 days |
| 2000-03-24 → 2002-10-09 | 49.1% | 929 days |
| 1973-01-11 → 1974-10-03 | 48.2% | 630 days |
| 1968-11-29 → 1970-05-26 | 36.1% | 543 days |
| 2020-02-19 → 2020-03-23 | 33.9% | 33 days |
| 1987-08-25 → 1987-12-04 | 33.5% | 101 days |
| 1961-12-12 → 1962-06-26 | 28.0% | 196 days |
| 1980-11-28 → 1982-08-12 | 27.1% | 622 days |
| 2022-01-03 → 2022-10-12 | 25.4% | 282 days |
| 1966-02-09 → 1966-10-07 | 22.2% | 240 days |

> ✅ **Pick: Median drawdown ≈ 8% (7.99%, ~8%)**
> ✅ Median duration ≈ **40 days** from peak to trough (if asked)

---

## Question 4 — AMZN Earnings Surprises

- 25 earnings dates from 2020-10-29 (1 future date excluded → 24 valid)
- 20 positive surprises, 4 negative surprises

| Metric | Value |
|---|---|
| **Median 2-day return after POSITIVE surprises** | **≈ +0.35%** (very slightly positive) |
| Correlation (Surprise % ↔ 2-day return) | **≈ 0.22** (weak positive correlation) |
| Median 2-day return (ALL events) | −0.17% |
| Median 2-day return (NEGATIVE surprises) | −1.13% |

> ✅ **Pick: Median 2-day return ≈ 0.3–0.5%** (choose the option closest to ~0.35%)
> ✅ Correlation ≈ **0.22** (weak positive)

> **Note:** The correlation is weak because several large positive surprises (e.g., 2022-10-27 +33% surprise → −10.6% return; 2024-08-01 +24% surprise → −10.2% return) were followed by "sell-the-news" reactions, while the largest beats (2022-02-03 +642%, 2026-07-30 +215%) rallied hard.

---

## Question 5 (free text) — Capstone Idea

> *"I want to build a **short-term (1–2 week) return prediction model for large-cap US tech stocks (AAPL, MSFT, GOOGL, AMZN, NVDA, META)**. I will combine technical indicators (RSI, MACD, Bollinger Bands, 20-day momentum), earnings surprise magnitude, VIX levels, and sector ETF flows as features. I'll train an XGBoost classifier to predict the direction of 5-day forward returns and evaluate via walk-forward validation, then compare against a simple buy-and-hold benchmark."*

---

## Question 6 (free text) — Additional Metrics

- **VIX (^VIX)** — volatility regime affects post-earnings drift and drawdown depth.
- **US 10-Year Treasury Yield (^TNX)** — rising rates compress growth/tech valuations.
- **DXY US Dollar Index** — impacts multinational revenue translation (relevant for AMZN, AAPL).
- **Sector ETFs (XLK, XLF, XLE)** — capture sector rotation / macro regime.
- **FRED macro series (UNRATE, CPI, FEDFUNDS)** via `pandas_datareader` for macro context.
- **Put/Call ratio & AAII sentiment** — sentiment contrarian signals.
- Retrieve all via `yfinance` (tickers like `^VIX`, `^TNX`, `DX-Y.NYB`) or `pandas_datareader.get_data_fred()`.

---

## 🎯 Quick Answer Key (for the form)

| Question | Answer |
|---|---|
| **Q1** | **2025** |
| Q1 additional | **~224** (or 218 if "≤ 2005") |
| **Q2** | **2** indices beat S&P 500 YTD |
| **Q3** | **Median drawdown ≈ 8%** (~7.99%) |
| **Q4** | **Median 2-day return ≈ 0.35%**; correlation ≈ **0.22** |

---

## Files in this repository

| File | Description |
|---|---|
| `README.md` | This file — answers and explanations |
| `homework1_solutions.ipynb` | Complete Jupyter notebook with code for all questions |
| `Module01_Colab_Introduction_and_Data_Sources.ipynb` | Original course reference notebook |
