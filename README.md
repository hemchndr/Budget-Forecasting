## Budget Forecasting for Apple Inc. Using Time Series Analysis
**Project Overview**
This project aims to forecast the future values of "Cash & Equivalents" for Apple Inc. using historical financial data. The dataset comprises annual financial metrics from 2012 to 2021. We explore two primary forecasting models: ARIMA and Prophet, to determine which provides the best forecast accuracy and reliability.

**Data Description**
The dataset contains financial data for Apple Inc., with columns representing various financial metrics over multiple years. For this project, we focus on the "Cash & Equivalents" metric.

**Dataset Columns:**

Metric: Type of financial metric
2012 to 2021: Annual values for each metric
Selected Metric:

Cash & Equivalents
**Steps Performed**
**1. Data Loading and Preprocessing**
Loaded the dataset and converted it from wide to long format for easier manipulation.
Filtered the dataset to focus on the "Cash & Equivalents" metric.
Converted the 'Year' column to datetime format and set it as the index.
Ensured there were no missing or NaN values.

**2. Exploratory Data Analysis (EDA)**
Statistical Summary: Provided basic statistics to understand the data's central tendency and variability.
Line Plot with Moving Averages: Visualized the data along with 3-year and 5-year moving averages to identify trends.
Autocorrelation and Partial Autocorrelation Plots: Used to help identify the order of AR and MA components for the ARIMA model.

**3. Model Selection and Training**

**ARIMA Model**
Model Configuration: Attempted different ARIMA configurations (ARIMA(1, 1, 1) and ARIMA(1, 1, 0)).
Diagnostics: Checked model diagnostics to ensure residuals were normally distributed and free from significant autocorrelation.
Results for ARIMA(1, 1, 0):

Log Likelihood: -73.002
AIC: 150.005
BIC: 150.399
Model Coefficients: AR(1) coefficient was not statistically significant.

**Prophet Model**

Model Configuration: Initialized and fitted the Prophet model using historical data.
Forecasting: Created a future dataframe and predicted future values.

**4. Forecasting and Visualization**

Forecasting Period: Forecasted for the next 5 years.
Visualization: Plotted the observed data along with forecasted values and confidence intervals.
