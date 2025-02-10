# Investigating Causal Relationships between Unemployment Rate and CPI using RStudio

In this project, we examine two key indicators: the unemployment rate and the consumer price index, from 2004 to the present, highlighting their interactions and interdependencies. Our analysis is based on the Phillips curve hypothesis, which posits an inverse relationship between unemployment and inflation in the short term. According to this theory, a decline in unemployment leads to higher wages and, consequently, an increase in inflation. However, the influence of structural and cyclical factors—such as economic recessions, the European Central Bank's monetary policies, and changes in labor market dynamics—has made this relationship more complex over time.

Our project aims to econometrically model this correlation to better understand the determinants and limitations of this relationship. After selecting seasonally adjusted time series for inflation and unemployment, we will conduct a comprehensive statistical and econometric analysis. This will include univariate modeling for each indicator, followed by testing a multivariate VAR model to examine their interactions. Our objectives are to verify the stationarity of the series, determine the most suitable model for each variable, and quantify the impact of a shock in one variable on the other. Finally, we will compare our results with theoretical expectations and contemporary developments in the inflation-unemployment relationship.
We divided this project into two main parties:

1. Univariate analysis:
   
   A)Unit Root and Stationarity Tests:
   - Augmented Dickey-Fuller (ADF) Test:
     The CPI series was found to be stationary, meaning it does not exhibit long-term trends.
     The unemployment rate series was non-stationary, indicating a persistent trend over time.
   - KPSS Test:
     The CPI series confirmed its stationarity.
     The unemployment rate test results were inconsistent with ADF, but graphical analysis supported its non-stationary nature.
     
   B)Homoscedasticity and Autocorrelation Tests
   - Ljung-Box Test for Residual Autocorrelation:
     No significant autocorrelation was found, indicating that the chosen model adequately captures the time series dynamics.
    - ARCH Test (Engle's Test for Heteroscedasticity):
      No presence of volatility clustering, meaning residuals are homoscedastic (constant variance over time).
    - Jarque-Bera Normality Test for Residuals:
      Residuals followed a normal distribution, validating the assumption of normality for the chosen models.
      
   C)Model Selection and Estimation
    An ARMA model was selected for the CPI series based on information criteria (AIC and BIC).
    The estimated model effectively captured price index fluctuations, with all coefficients statistically significant.
   
2. Multivariate Analysis:
   
  A)Vector Autoregression (VAR) Model:
    A VAR model was estimated to analyze the dynamic relationship between inflation and unemployment.
    The results showed that past values of CPI significantly influence the unemployment rate, supporting theoretical expectations.
    However, past values of unemployment had little impact on inflation.
    
  - Johansen Cointegration Test:
      No long-term equilibrium relationship was found between inflation and unemployment, implying short-term interactions but no stable long-run link.
      
   B)Impulse Response and Forecasting
   - Impulse Response Analysis:
      CPI fluctuations have a stronger impact on the unemployment rate than vice versa.
      Economic shocks to inflation influence unemployment, but the effect is not symmetric.
  - Forecasts:
      Predictions suggest moderate fluctuations in inflation over the next quarters, aligning with recent economic trends.

Conclusion:
The study confirms that inflation follows a stationary process, while unemployment is non-stationary. The ARMA model provides a reliable fit for inflation, and the VAR model highlights significant short-term interactions between inflation and unemployment. However, the absence of cointegration suggests no stable long-term relationship between the two variables. These findings contribute to understanding the short-term tradeoff between inflation and unemployment in France.













