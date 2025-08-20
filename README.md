# Volatility-Forecasting-using-GARCH
A Classical vs. Machine Learning Approach on S&amp;P 500 Data

In my project, I explored modeling volatility in stock returns using ARCH and GARCH models. Financial returns often exhibit volatility clustering — periods of calm followed by turbulence — which standard mean models like ARIMA cannot capture.

I started by computing daily percentage returns and checking for autocorrelation using the Ljung-Box test and for heteroskedasticity using Engle’s ARCH test. Both confirmed volatility clustering, so GARCH was appropriate.

I then estimated a GARCH(1,1) model, where the variance today depends on both yesterday’s squared shock and yesterday’s variance. I interpreted the parameters: α captures the immediate impact of shocks, β measures persistence, and ω is the baseline variance. My model showed moderate persistence in volatility, consistent with financial market behavior.

I also ran diagnostic checks like Shapiro-Wilk for normality of residuals and experimented with higher-order GARCH models through a grid search. This highlighted the challenge of fitting volatility in individual stocks, which often have jumps.

Overall, this project taught me how to rigorously model and forecast risk, which is highly relevant for roles in risk management and quantitative finance, where volatility modeling underpins Value-at-Risk, option pricing, and portfolio optimization.

As an extension to thsi project, I worked on forecasting the volatility of Repsol’s stock. Volatility is crucial in risk management and trading, so I wanted to compare two very different approaches. First, I applied GARCH, which is a classical time-series model specifically designed to capture volatility clustering. Then, I trained an XGBoost machine learning model to predict rolling monthly volatility.

What I found was that while GARCH explained volatility well in-sample, XGBoost gave better out-of-sample forecasts. The project really helped me understand volatility as a time-varying measure of risk, how to evaluate models on forecasting accuracy, and the trade-offs between classical econometric approaches and modern ML.

For me, the big takeaway was that in quant/risk work, it’s not about picking one tool — it’s about knowing the strengths of each and applying the right one depending on the context.
