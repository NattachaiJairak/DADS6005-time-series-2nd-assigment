# DADS6005-time-series-2nd-assigment

# Time Series Forecasting with Holt-Winters Exponential Smoothing

This project demonstrates the application of Holt-Winters exponential smoothing for forecasting total sales data. The project is implemented in Python using libraries such as Pandas, Matplotlib, Statsmodels, and Scikit-learn.

## Project Overview

The project involves the following steps:

1. **Data Import and Exploration:**
   - Import sales data from an Excel file using Pandas.
   - Perform exploratory data analysis to understand the data's characteristics, including shape, information, descriptive statistics, and visualization.

2. **Time Series Decomposition:**
   - Decompose the time series into trend, seasonal, and residual components using the `seasonal_decompose` function from Statsmodels.
   - Visualize the decomposed components to gain insights into the data's patterns.

3. **Data Splitting and Frequency Setting:**
   - Split the data into training and testing sets (80% for training, 20% for testing).
   - Set the frequency of the time series index to monthly.

4. **Model Fitting, Prediction, and Evaluation:**
   - Fit Holt-Winters exponential smoothing models with different configurations of trend and seasonality.
   - Forecast total sales for the test period.
   - Evaluate model performance using metrics such as Mean Absolute Error (MAE) and Mean Squared Error (MSE).

5. **Conclusion:**
   - Based on the evaluation results, select the best-performing model configuration.
   - Provide insights and conclusions regarding the chosen model's performance and suitability for the data.

## Dataset

The dataset used in this project contains monthly total sales data. It is sourced from an Excel file located at:

'https://github.com/NattachaiJairak/DADS6005-time-series-2nd-assigment/raw/main/S12_44.xlsx'

## Libraries Used

The project utilizes the following libraries:

- Pandas
- Matplotlib
- Statsmodels
- Scikit-learn

## Results

The project's results show that the model with multiplicative trend and multiplicative seasonality (`trend='mul', seasonal='mul'`) achieved the best forecast accuracy, with the lowest MAE and MSE values. This indicates that both trend and seasonality are better captured by multiplicative components.

## Conclusion

Holt-Winters exponential smoothing is an effective technique for forecasting time series data. This project demonstrated the process of applying this technique to total sales data, including data exploration, model fitting, prediction, and evaluation. The results highlighted the importance of selecting an appropriate model configuration to achieve accurate forecasts.

# Holt-Winter Exponential Smoothing
2nd Assignment - Moving Average &amp; Simple Expo Smoothing.Try to answer what is the best model (lower forecast error).
Here is a config of model fitting.
    1. {'trend': 'add', 'seasonal': 'add'}
    2. {'trend': 'add', 'seasonal': 'mul'}
    3. {'trend': 'mul', 'seasonal': 'add'}
    4. {'trend': 'mul', 'seasonal': 'mul'}
# Interpretaion and Conclusion 
**1. Model (trend=add, seasonal=add): MAE = 200.17, MSE = 61690.11**
This model uses an additive trend and additive seasonality. While it provides a reasonable forecast, its MAE and MSE are higher than some of the other models, indicating that it may not capture the data patterns as well.

**2.Model (trend=add, seasonal=mul): MAE = 222.19, MSE = 73579.47**
This model uses an additive trend and multiplicative seasonality. It performs slightly worse than the first model, with higher MAE and MSE values, indicating that this configuration may not be ideal for your data.

**3.Model (trend=mul, seasonal=add): MAE = 123.92, MSE = 24785.76**
This model uses a multiplicative trend and additive seasonality. It performs significantly better than the additive trend models, with much lower MAE and MSE values. This suggests that using a multiplicative trend helps in capturing the data's underlying pattern more accurately.

**Model (trend=mul, seasonal=mul): MAE = 102.32, MSE = 15637.04**
This model, which uses both multiplicative trend and multiplicative seasonality, has the lowest MAE and MSE among all models, indicating that it provides the most accurate forecast.

**Conclusion**
The model with multiplicative trend and multiplicative seasonality (trend=mul, seasonal=mul) provides the best forecast for your data, as it has the lowest MAE (102.32) and MSE (15637.04). This suggests that both the trend and seasonal components of your data are better represented by a multiplicative approach, which may capture variations in both trend and seasonality more effectively. This model would be the best choice based on your forecast accuracy criteria.
