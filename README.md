MSc Business Analytics dissertation project forecasting UK clothing retail sales using Seasonal Naïve, SARIMA and SARIMAX models.
# UK Clothing Retail Sales Forecasting

## Project Overview

This repository contains the data and Python analysis developed for an MSc Business Analytics dissertation examining the forecasting of UK clothing retail sales.

The study investigates whether traditional time-series models and external indicators can improve forecasting accuracy for UK clothing retail sales. Seasonal Naïve, SARIMA and SARIMAX forecasting approaches are evaluated using monthly data from 2015 to 2025.

## Research Objective

The objective of the study is to analyse historical patterns in UK clothing retail sales and assess whether external indicators, including Clothing CPI and Google Trends search-interest variables, provide additional predictive information for forecasting clothing demand.

## Dataset

The analysis uses monthly data covering January 2015 to December 2025.

The main variables include:

- **Sales_volume** – non-seasonally adjusted UK textile, clothing and footwear retail sales volume index
- **Clothing_CPI** – UK Clothing and Footwear Consumer Price Index
- **Winter_Coats** – Google Trends search interest
- **Summer_Dresses** – Google Trends search interest
- **Black_Friday_Clothing** – Google Trends search interest
- **School_Uniform** – Google Trends search interest

The retail sales and CPI data were obtained from the UK Office for National Statistics (ONS), while search-interest indicators were obtained from Google Trends.

## Methodology

The forecasting analysis includes:

- Exploratory time-series analysis
- Correlation and multicollinearity assessment
- Augmented Dickey-Fuller (ADF) stationarity testing
- First differencing
- ACF and PACF analysis
- Seasonal Naïve benchmark forecasting
- SARIMA candidate-model comparison
- Rolling-origin validation
- SARIMA forecasting
- SARIMAX modelling using external indicators
- Out-of-sample forecast evaluation

The data were divided chronologically into a training period from January 2015 to December 2024 and a held-out testing period from January to December 2025.

Model selection was conducted without using the 2025 test observations. Rolling-origin validation across 12 monthly forecast origins in 2024 was used to support model selection.

## Final Forecasting Results

Out-of-sample forecasting performance on the 2025 test period was:

| Model | MAE | RMSE | MAPE |
|---|---:|---:|---:|
| Seasonal Naïve | 3.825 | 4.847 | 3.81% |
| SARIMAX | 5.267 | 6.251 | 5.37% |
| SARIMA | 7.216 | 7.864 | 7.49% |

The Seasonal Naïve model achieved the lowest forecasting errors across all three evaluation metrics.

The SARIMAX model improved upon the SARIMA model, suggesting that the selected Google Trends indicators provided some additional predictive information. However, the inclusion of these external indicators was not sufficient to outperform the Seasonal Naïve benchmark during the 2025 test period.

## Repository Contents

- **Master Dataset** – final dataset used for the forecasting analysis
- **UK_Clothing_Retail_Forecasting_NSA.ipynb** – executed Python notebook containing data preparation, analysis, model development, validation and forecast evaluation
- **README.md** – overview of the project, data and methodology

## Software and Libraries

The analysis was conducted in Python using libraries including:

- pandas
- numpy
- matplotlib
- statsmodels
- scikit-learn

## Notes

The SARIMAX evaluation uses observed external-variable values for the 2025 test period. In a real-world future forecasting setting, these external indicators would themselves need to be known or forecast in advance.

This repository is provided as supporting analytical material for an MSc Business Analytics dissertation.
