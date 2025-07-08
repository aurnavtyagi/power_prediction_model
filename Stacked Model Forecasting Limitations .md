#  Stacked Model Forecasting Limitations

This document outlines the known limitations of the **stacked ensemble forecasting model** used in this project (XGBoost + LightGBM + CatBoost).

---

##  Key Limitation: Effective Only for 6–12 Hour Predictions

The stacked model is designed for **short-term forecasting only**. It produces reliable forecasts **up to 6–12 hours**, after which:

- Accuracy sharply decreases.
- Predictions become **flat or regressed to the mean**.
- Temporal patterns vanish beyond short horizons.

---

##  Why This Happens

### 1. Limited Historical Data (Only 4 Years)

- The model is trained on just **4 years of power generation data**.
- This limits its ability to learn **seasonal**, **holiday**, or **anomaly-driven** trends.
- It also can't generalize well to **unseen future scenarios**.

### 2. No Weather or External Context

- **No weather API or meteorological features** are included.
- Power generation (especially in dams) is **highly weather-dependent** (rainfall, temperature, snowmelt, etc.).
- Without these, the model **misses key context**, leading to generic, flat predictions.

### 3. Lag Feature Dependency

- The model relies heavily on **lag features** like:
  - Power at t–1, t–2, t–3, ..., t–96 (i.e., past 24 hours)
- These work well when actual recent data is known.
- But in multi-step forecasting (e.g., 15-min intervals for the next 24 hours), **we feed predicted values back into the model** (recursive forecasting).
- This causes **compounding error** and leads to inaccurate results.


## ✅ What It Does Well

- Fast and interpretable
- Ideal for **operational planning within a few hours**
- Easy to debug and deploy
- Works well with clean historical time series

---

## What You Should Avoid

- Using it for long-term (>1 day) planning
- Assuming it learns seasonality or holidays
- Treating outputs beyond 12 hours as trustworthy

---



## 📎 Summary

The current stacked ensemble is best used for **short-term (6–12 hours)** forecasting due to:

- Lack of weather data
- Limited historical coverage (only 4 years)
- Lag-based, memory-less architecture

It is **not suitable** for long-range or climate-driven power prediction.

---
