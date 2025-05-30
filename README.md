# Air-Quality-Prediction-Using-Time-Series-Analysis

## Project Description
This project predicts hourly averaged concentrations of air pollutants (CO, NMHC, Benzene, NOx, NO2) for the next 48 hours using a dataset of chemical sensor responses. It utilizes time series modeling and RMSE validation to ensure accuracy, incorporating data preprocessing and feature engineering to improve forecast reliability.

## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling Approach](#modeling-approach)
- [Forecasting and Validation](#forecasting-and-validation)
- [Final Prediction](#final-prediction)
- [Residual and Error Analysis](#residual-and-error-analysis)
- [Feature Engineering Insights](#feature-engineering-insights)
- [Conclusion](#conclusion)
- [Technologies Used](#technologies-used)
- [License](#license)

## Introduction
The aim of this project is to predict the future 48 hours of hourly averaged concentrations for major air pollutants and related environmental factors. Accurate short-term air quality predictions are crucial for public health and environmental planning.

## Data Preprocessing
1. **Missing Values**: Utilized a sentinel value (-200) to mark missing readings, converted to NaN, and processed through imputation.
2. **Datetime Management**: Combined Date and Time columns into a single timestamp column for better time-series operations.
3. **Indexing and Interpolation**: Reindexed data by hourly timestamps and filled remaining gaps using linear interpolation.

## Exploratory Data Analysis
- **Time-Series Plots**: Analyzed trends, seasonality, and anomalies in pollutant levels.
- **Distribution Checks**: Used histograms and boxplots to understand variable distributions and identify outliers.
- **Correlation Analysis**: Calculated correlation matrices to uncover relationships between pollutants and environmental variables.

## Modeling Approach
- **ARIMA Models**: Employed AutoRegressive Integrated Moving Average for forecasting stationary series.
- **Prophet Model**: Used Facebook's Prophet for its robustness against missing data and ability to capture multiple seasonalities.

## Forecasting and Validation
- Divided data into training (90%) and validation (10%) sets.
- Created forecasts during the validation period and compared them to actual values.
- Measured accuracy using Root Mean Square Error (RMSE).

## Final Prediction
After validating models, retrained the best-performing ARIMA and Prophet models on the entire dataset to predict pollutant concentrations and weather parameters for the next 48 hours.

## Residual and Error Analysis
- **Autocorrelation**: Analyzed residuals to ensure they resembled white noise.
- **Normality**: Checked residual distributions for normality using histograms and QQ-plots.
- **Error Distribution**: Calculated summary statistics of residuals to confirm model adequacy.

## Feature Engineering Insights
- Incorporated lag variables and time indicators to enhance model inputs.
- Explored the impact of time-based features on prediction accuracy.

## Conclusion
The project successfully demonstrated an end-to-end time-series forecasting pipeline for multivariate air quality data. Future research may explore ensemble or deep-learning approaches to improve predictions further.

## Technologies Used
- Python
- Pandas
- NumPy
- Statsmodels
- Facebook Prophet
- Matplotlib
- Seaborn
