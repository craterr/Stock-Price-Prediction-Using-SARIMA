# Dane Street Investment Firm - Stock Market Prediction Challenge
## (Kaggle Competition)

## Task Overview

Your team at Dane Street, a prominent investment firm, has been tasked with predicting the future performance of a specific stock for High Net-worth Individuals (HNIs). The goal is to provide close price predictions and recommend the best strategy (Buy, Sell, or Hold) for each day.

Your team has identified a stock that seems to performing well and you clients want to know more before they commit their millions to your call. Thus your task is two-fold. First, you need to predict the close prices of the stock in question. Further, you need to suggest the best strategy for your client on any given day. There are three options your clients have. They can either Buy, Hold or Sell the stock. Your team needs to suggest the best decision.

## Dataset Description
The dataset `train.csv` consists of weekly stock price data from June 1, 2015 to Feb 22, 2021. It contains the Open price, Close price, Volume and Strategy of all the stocks traded in that time interval. Your objective is to predict the Close price and Strategy of stocks on the `test.csv` sample.

## Files
`train.csv` - the training set for the model
`test.csv` - the test set on which performance will be judged

## Data Dictionary

- **Date** - Date in date time format
- **Open** - Open price of the stock for that week
- **Close** - Close price of the stock for that week
- **Volume** - The number of shares of that stock traded that week
etc.




## Evaluation Metrics

### Close Price Prediction (SMAPE)

The Symmetric Mean Absolute Percentage Error (SMAPE) will be used to evaluate close price predictions.

![image](https://github.com/craterr/Stock-Price-Prediction/assets/106965125/5a6fcf04-d60d-4258-8d3f-da429e26967f)

```python
smape = np.mean(np.abs(y_pred - y_true) / (np.abs(y_pred) + np.abs(y_true)))
```
### Strategy Prection (Accuracy)
The Strategy will be evaluated using Accuracy.

```python
accuracy = sklearn.metrics.accuracy_score(y_true, y_pred) * 100
```
