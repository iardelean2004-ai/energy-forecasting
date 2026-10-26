# Hourly Energy Consumption Forecasting: XGBoost vs LSTM

Day-ahead forecasting of hourly electricity demand (PJM East), comparing a naive baseline, XGBoost and an LSTM.

## Results
| Model | MAE (MW) | RMSE (MW) | MAPE |
|---|---|---|---|
| Baseline | 3,400 | 4,645 | 10.54% |
| LSTM | 2,112 | 2,837 | 6.72% |
| XGBoost | 1,793 | 2,421 | 5.63% |

## Data
[PJM Hourly Energy Consumption (Kaggle)](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption).
Download `PJME_hourly.csv` and place it next to the notebook.

## Run
pip install -r requirements.txt, then open energy.ipynb (Python 3.12).

## Method
Chronological split (train ≤ 2013, validation 2014, test 2015+), no data leakage. Features use only information available 24h ahead.
