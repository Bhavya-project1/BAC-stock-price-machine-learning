# Bank of America (BAC) Stock-Price Modelling with Machine Learning

A machine-learning project focused on modelling the historical stock price of **Bank of America Corporation (NYSE: BAC)**.

## Project Objectives

- Obtain and inspect historical BAC market data.
- Prepare data for supervised machine-learning analysis.
- Explore relationships between market features and the target variable.
- Train and evaluate the model implemented in the notebook.
- Examine observed versus model-estimated values.

## Implementation

The main implementation is in `BAC_prediction_using_machine_learning.ipynb`. Refer to the notebook for the exact feature set, algorithm, train/test design, hyperparameters, and evaluation metrics.

## Technology

Python · Jupyter Notebook · pandas · NumPy · Machine-learning libraries used in the notebook

## Run

Open the notebook in Jupyter or Google Colab. A common starting environment is:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn yfinance jupyter
jupyter notebook
```

Install any additional packages imported by the notebook. External market-data retrieval may require an internet connection and may produce updated observations.

## Evaluation Notes

Stock-price modelling is vulnerable to overfitting, look-ahead bias, and non-stationarity. Use chronological validation, document the forecast horizon, compare with naïve price and return baselines, and report out-of-sample error metrics. Predictive accuracy alone does not imply economic value or trading profitability.

## Disclaimer

Educational modelling exercise only. Not investment advice or a recommendation to trade BAC shares.
