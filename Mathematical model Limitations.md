# Forecasting Model Limitations

This repository contains a time-series mean-based forecasting model for predicting power generation at 15-minute intervals.

## ⚠️ Key Limitation: Single-Year Forecast Only

The current implementation is designed to generate accurate forecasts **only for the immediate target year** (e.g., 2026). The model leverages historical patterns from the previous 4 years to predict one month at a time.

### Why only 1-year?

- It relies on averaging values from **the same day and time across the last 4 years**.
- There is **no mechanism** for generating synthetic future values beyond the next year.
- Long-term patterns (like changing climate, dam operations, or policy changes) are **not captured** in this basic averaging method.

## 🚫 What this model is NOT:

- ❌ It is NOT a multi-year forecast model.
- ❌ It does NOT use deep learning or autoregressive methods like LSTM or ARIMA.
- ❌ It does NOT model trend or seasonality beyond local past patterns.

## ✅ What it does well:

- ✅ Accurately predicts **monthly or daily power generation** for the immediate next year.
- ✅ Useful for short-term planning, comparisons, or sanity checks.
- ✅ Lightweight and interpretable.

---


