# Volatility-Forecasting-using-GARCH
A Classical vs. Machine Learning Approach on S&amp;P 500 Data

## 🔹 Overview

* Project on **modeling and forecasting stock return volatility**.
* Compared **classical econometric models (ARCH/GARCH)** with a **machine learning approach (XGBoost)**.
* Data used:

  * **S\&P 500 stock returns** (for GARCH modeling)
  * **Repsol stock returns** (for volatility forecasting)

---

## 🎯 Motivation

* Volatility = key measure of **financial risk**.
* Standard mean models (e.g., ARIMA) fail to capture **volatility clustering**.
* **GARCH** → interpretable, risk-focused.
* **XGBoost** → captures nonlinear patterns, better forecasting power.

---

## ⚙️ Methodology

### Part I – ARCH & GARCH (S\&P 500)

* Computed **daily percentage returns**.
* Tests:

  * **Ljung-Box** → autocorrelation
  * **Engle’s ARCH** → heteroskedasticity
* Fit **GARCH(1,1)** model:

  * ω → baseline variance
  * α → immediate impact of shocks
  * β → persistence of volatility
* Ran residual diagnostics + experimented with higher-order GARCH.

### Part II – GARCH vs XGBoost (Repsol)

* Created **rolling monthly volatility** (std dev of returns).
* Fit **GARCH model** → in-sample explanation.
* Trained **XGBoost Regressor** → out-of-sample forecasting.
* Compared based on **forecasting accuracy**.

---

## 📊 Key Findings

* Volatility clustering confirmed → **GARCH suitable**.
* **GARCH(1,1)** showed moderate persistence (β close to 1).
* **XGBoost outperformed GARCH** for out-of-sample forecasts.
* Takeaway: **Use both tools depending on context** (interpretability vs accuracy).

---

## 🧑‍💻 Tools & Libraries

* Python: `pandas`, `numpy`, `statsmodels`, `arch`, `scipy`, `xgboost`, `matplotlib`
* Econometric Tests: Ljung-Box, Engle’s ARCH, Shapiro-Wilk

---

## ✅ Learning Outcomes

* Understood **volatility as time-varying risk**.
* Hands-on with **ARCH/GARCH modeling**.
* Applied **ML (XGBoost) to financial time series**.
* Balanced **interpretability vs prediction** in quant/risk modeling.

---

## 🚀 Extensions

* Try **EGARCH / GJR-GARCH** (asymmetry, leverage effect).
* Explore **LSTMs** for sequential forecasting.
* Extend to **multi-asset portfolios**.

---


