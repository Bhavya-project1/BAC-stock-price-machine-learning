# Bank of America Stock-Price Modelling with Machine Learning

A supervised-learning exercise that models the daily closing price of **Bank of America (BAC)** using historical price information from financial peers and broader market indicators.

## Data and Features

The notebook downloads daily market data for the period **2002-01-01 to 2025-01-01** for:

| Category | Instruments / indicators |
|---|---|
| Target | Bank of America (BAC) |
| Banking peers | JPM, MS, Citigroup (C), Wells Fargo (WFC) |
| Market proxy | SPY |
| Volatility | VIX |
| Interest rates | US 10-year Treasury yield (^TNX) |
| Macro / commodities | US Dollar Index, crude-oil futures, gold futures |

The feature-engineering workflow uses lagged peer and market variables, BAC moving averages (5-day and 10-day), and a lagged five-day BAC percentage change. The target is the BAC closing price.

## Models Compared

- Decision Tree Regressor
- Random Forest Regressor
- K-Nearest Neighbours Regressor
- Support Vector Regressor

The notebook uses a chronological 90% / 10% train-test split (shuffle=False) and compares models using R², mean squared error (MSE), root mean squared error (RMSE), and actual-versus-predicted plots.

## Repository Contents

- BAC_prediction_using_machine_learning.ipynb — complete implementation.

## Technology

Python · NumPy · pandas · yfinance · Matplotlib · Plotly · scikit-learn

## Run

~~~bash
pip install -r requirements.txt
jupyter notebook
~~~

Open the notebook and execute the cells in sequence. The notebook retrieves data at runtime, so results may vary with provider updates.

## Research Limitations and Next Steps

The current target is a price level, which is persistent and can make price-level metrics look stronger than true predictive performance. A stronger study should include a previous-close benchmark, predict returns or price changes, scale features for distance/kernel-based models, tune hyperparameters using time-series validation, and report model performance across multiple rolling test periods. Lag construction and missing-data handling should also be reviewed for each asset independently.

Model fit is not evidence of a profitable strategy. Execution costs, forecast-to-signal conversion, and portfolio-level evaluation would be required for an investment claim.

## Disclaimer

Educational machine-learning project only. Not investment advice or a recommendation to trade BAC.
