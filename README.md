# Time Series Forecasting of Daily Sales using ARIMA

This project performs time series forecasting on daily sales data using the ARIMA model. It includes preprocessing steps such as normalization and outlier handling to improve prediction accuracy.

## Project Overview

- **Objective:** Predict future daily sales using historical sales data.
- **Approach:** ARIMA model with preprocessing and evaluation using MAE and RMSE metrics.
- **Tools Used:** Python, Pandas, Matplotlib, statsmodels

## Dataset

The dataset contains historical daily sales with the following columns:

- `OrderDate`: Date of sale (used as time index)
- `total_qty_sales`: Total quantity of items sold (target variable)
- `Selling Price`: Selling price for the day (not used for modeling)

**Target Column for Forecasting:** `total_qty_sales`


## Preprocessing

1. **Datetime Parsing:** Converted `OrderDate` to datetime and set as index.
2. **Resampling:** Grouped data by day to ensure regular time series format.
3. **Outlier Removal:** Clipped outlier values using IQR method.
4. **Normalization:** Scaled the sales column using `MinMaxScaler` for better model performance.
5. **Train-Test Split:** 80% for training, 20% for testing.


## Model Used

### ARIMA (AutoRegressive Integrated Moving Average)

- **Order (p,d,q):** Chosen as (5,1,0) after basic analysis
- **Why ARIMA?** Suitable for non-seasonal time series with trends and patterns.

## Evaluation

**Metrics Used:**
- **MAE (Mean Absolute Error):** `187.42`
- **RMSE (Root Mean Squared Error):** `269.97`

I have also plot graph of actual vs predicted testing sample for better understanding. 
