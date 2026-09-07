# Sales-Forecasting
# 📈 Sales Forecasting Using Time Series Analysis

## 📌 Project Overview

This project focuses on forecasting future sales using historical monthly sales data and time series forecasting techniques.

The objective was to analyze sales patterns, identify seasonality, build multiple forecasting models, evaluate their performance, and select the best-performing model for predicting future sales.

---

## 🎯 Project Objectives

* Analyze historical monthly sales trends
* Identify seasonal sales patterns
* Build baseline and time series forecasting models
* Compare model performance using evaluation metrics
* Select the best forecasting model
* Forecast sales for the next 12 months

---

## 📊 Dataset

The dataset contains historical sales data aggregated at a monthly level.

* **Total Period:** 48 months
* **Training Data:** January 2015 – December 2017
* **Testing Data:** January 2018 – December 2018
* **Forecast Period:** January 2019 – December 2019

---

## 🔍 Exploratory Data Analysis

The sales data was analyzed to understand:

* Monthly sales trends
* Yearly patterns
* Seasonal variations

The analysis revealed strong seasonal behavior in sales.

Sales were generally higher during the later months of the year, particularly between **September and December**.

---

## 🤖 Forecasting Models

Three forecasting approaches were evaluated.

### 1. Naive Forecast

The Naive model uses the last observed sales value as the forecast for future periods.

This model was used as a baseline for comparison.

### 2. ARIMA

ARIMA (AutoRegressive Integrated Moving Average) was used to capture historical trends and relationships between previous observations.

Model configuration:

```text
ARIMA (1,1,1)
```

### 3. SARIMA

SARIMA (Seasonal AutoRegressive Integrated Moving Average) extends ARIMA by incorporating seasonal patterns.

Model configuration:

```text
SARIMA (1,1,1)(1,1,1,12)
```

The seasonal period of **12** was used because the dataset contains monthly sales data.

---

## 📏 Model Evaluation

The models were evaluated using:

* **MAE (Mean Absolute Error)** – Average prediction error
* **RMSE (Root Mean Squared Error)** – Measures prediction error while penalizing larger errors
* **MAPE (Mean Absolute Percentage Error)** – Average prediction error expressed as a percentage

---

## 🏆 Model Performance

| Model      |           MAE |          RMSE |       MAPE |
| ---------- | ------------: | ------------: | ---------: |
| Naive      |     39,267.96 |     43,945.62 |     98.73% |
| ARIMA      |     23,158.21 |     26,996.79 |     53.62% |
| **SARIMA** | **13,930.02** | **16,394.82** | **27.77%** |

### 🥇 Best Model: SARIMA

SARIMA achieved the lowest error across all evaluation metrics and was selected as the final forecasting model.

The results demonstrate that incorporating seasonal patterns significantly improved forecasting accuracy.

---

## 🔮 2019 Sales Forecast

The final SARIMA model was trained using the complete historical dataset and used to forecast sales for the next 12 months.

### Key Forecast Insights

* Sales are expected to increase during the later months of the year.
* **September to December** are predicted to be the strongest sales periods.
* **November** is forecasted to have the highest sales.
* The forecast continues the seasonal pattern observed in the historical data.

---

## 📊 Visualizations

The project includes the following visualizations:

* Historical monthly sales trend
* Monthly seasonality analysis
* Actual Sales vs SARIMA Forecast
* Historical Sales and Future Sales Forecast

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Statsmodels
* Google Colab

---

## 📁 Repository Structure

```text
Sales-Forecasting/
│
├── Sales_Forecasting.ipynb
├── future_sales_forecast.csv
└── README.md
```

---

## 🚀 Conclusion

The project successfully developed and evaluated multiple time series forecasting models for sales prediction.

Among the models tested, **SARIMA outperformed both the Naive Forecast and ARIMA models**, achieving the lowest MAE, RMSE, and MAPE values.

The final model was used to generate a 12-month sales forecast, providing insights into expected seasonal sales patterns and future business performance.

---

⭐ If you found this project useful, feel free to explore the repository!
