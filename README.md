# 📈 UNVR Stock Forecasting with Prophet (2013–2017)
![Unilever Forecasting](Unilever_Forecasting.gif)

## 🔍 Project Overview
This project forecasts the stock price of **PT Unilever Indonesia Tbk (UNVR)** using **Prophet**, a powerful time series model developed by Meta. We applied hyperparameter tuning, time-based cross-validation, and rigorous visual evaluation to simulate real-world forecasting for investment scenarios.

> ✅ **Forecast Target**: UNVR stock price for the year 2017  
> 📅 **Training Period**: 2013–2016  
> 🧠 **Model Used**: Prophet (with/without tuning)
---

## 📊 Methodology

### 1. 📌 Exploratory Data Analysis (EDA)
- Trend & seasonality decomposition
- Rolling statistics and moving averages
- Holiday effects and changepoints detection

### 2. 🔮 Forecasting Models
- **Baseline Prophet Model** with default parameters
- **Tuned Prophet Model** using grid search on:
  - `changepoint_prior_scale`
  - `seasonality_mode`
  - `seasonality_prior_scale`

### 3. 📉 Cross-Validation Strategy
- `initial='730 days'` → 2-year training window
- `period='180 days'`  → Forecasting interval
- `horizon='365 days'` → 1-year prediction window
- Performance evaluated using MAPE, MAE, RMSE

---

## 📊 Forecast Summary

| Model              | Description                  | MAPE   | MAE    | RMSE   |
|-------------------|------------------------------|--------|--------|--------|
| **Baseline Prophet** | Default setting (no tuning) | 6.47%  | 425.13 | 577.42 |
| **Tuned Prophet**    | Grid search & optimization   | **1.25%** | **98.54**  | **121.77** |


> Tuning hyperparameters reduced MAPE by over **80%**, showing strong predictive gains, especially during volatile periods.

---

## 🖼️ Visual Evaluation

### 🔹 Baseline Model
- Captured early-year trends
- Underestimated Q4 price spike

### 🔸 Tuned Model
- Strong alignment with actual prices
- More accurate in volatile zones with tighter confidence bounds

---

## 💡 Key Insights

- **Prophet is effective** for medium-term stock trend prediction with proper tuning.
- Inclusion of external regressors and parameter control significantly **boosts accuracy**.
- Forecasting stock prices still faces challenges due to **market noise** and **non-linear events** — consider hybrid models in future work.

---

## 👥 Data Science Team

- [Ahmad Faik Setiawan](https://github.com/ahmadFaik)
- [Yora Okta Aviani Rahardjo](https://github.com/yoraoktaar)
- [Meriani Alexandra](https://github.com/jovellexa-code)
- [Ditya Ayu Anjani](https://github.com/Anjaani1)
- [Mauritz Labaro Lumban Gaol](https://github.com/mauritzlabora)
- [Kaila Amira Azzahra](https://github.com/filekeyholder)

---
