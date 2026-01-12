# 📈 U.S. Consumption Forecasting Using Time Series Models

---

## Project Overview
This project forecasts quarterly percentage changes in U.S. consumption
using historical macroeconomic indicators. The objective is to compare
traditional time series models with regression-based approaches that
incorporate external economic predictors.

---

## Business & Economic Context
Accurate consumption forecasts are critical for policy makers,
financial institutions, and economic planning. Consumption reflects
household confidence and economic health, making it a key macroeconomic
indicator.

---

## Data Description
The analysis uses the `uschange` dataset from the `fpp2` R package,
covering quarterly percentage changes from 1970 Q1 to 2016 Q3.

Key variables:
- Consumption
- Income
- Production
- Savings
- Unemployment

---

## Methodology
The following models were implemented and compared:

- ARIMA (univariate time series)
- ARIMAX with external regressors
- Multiple linear regression

Stationarity was assessed using ACF plots and Augmented Dickey–Fuller
tests. Model performance was evaluated using AIC, RMSE, MAE, and MAPE.

---

## Key Results
- Consumption is strongly influenced by Income and Unemployment
- ARIMAX models outperform pure ARIMA and linear regression
- The manually tuned ARIMAX(3,2,1)(1,0,1)[4] achieved the lowest AIC
- Forecast accuracy for the test period was high (RMSE ≈ 0.10)

---

## Forecast Performance

The selected ARIMAX model produces forecasts closely aligned with
observed consumption changes for the final 7 quarters.

---

## Limitations
- Residual autocorrelation remains mild
- Model does not capture external shocks
- Limited seasonality structure

---

## Conclusion
This project demonstrates the importance of incorporating economic
predictors into time series forecasting. ARIMAX models provide superior
performance when economic structure is present, while maintaining
interpretability.

---

## Tools Used
R • fpp2 • forecast • ggplot2 • tidyverse • tseries
