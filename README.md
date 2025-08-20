# Volatility-Forecasting-using-GARCH
A Classical vs. Machine Learning Approach on S&amp;P 500 Data

In my project, I explored modeling volatility in stock returns using ARCH and GARCH models. Financial returns often exhibit volatility clustering — periods of calm followed by turbulence — which standard mean models like ARIMA cannot capture.

I started by computing daily percentage returns and checking for autocorrelation using the Ljung-Box test and for heteroskedasticity using Engle’s ARCH test. Both confirmed volatility clustering, so GARCH was appropriate.

I then estimated a GARCH(1,1) model, where the variance today depends on both yesterday’s squared shock and yesterday’s variance. I interpreted the parameters: α captures the immediate impact of shocks, β measures persistence, and ω is the baseline variance. My model showed moderate persistence in volatility, consistent with financial market behavior.

I also ran diagnostic checks like Shapiro-Wilk for normality of residuals and experimented with higher-order GARCH models through a grid search. This highlighted the challenge of fitting volatility in individual stocks, which often have jumps.

Overall, this project taught me how to rigorously model and forecast risk, which is highly relevant for roles in risk management and quantitative finance, where volatility modeling underpins Value-at-Risk, option pricing, and portfolio optimization.
