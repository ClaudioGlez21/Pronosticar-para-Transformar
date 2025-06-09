# Forecasting for Transformation: A Time Series Analysis of Mexico's CO2 Emissions

![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)
![Libraries](https://img.shields.io/badge/libraries-pandas%2C%20statsmodels%2C%20matplotlib-orange)

## 📖 Project Overview

This repository contains a comprehensive time series analysis of Mexico's per capita CO2 emissions from 1970 to 2019. The project applies the Box-Jenkins methodology to identify a robust forecasting model, project future emissions, and critically evaluate these forecasts in the context of Mexico's climate commitments and the UN's Sustainable Development Goal 13 (Climate Action).

The core finding is that Mexico's historical emissions data shows significant inertia. The resulting forecast indicates a stabilization of emissions, a path that is insufficient to meet the nation's climate targets, highlighting a critical "implementation gap" that must be addressed through decisive policy action.

---

## 🎯 Project Objectives

The main goals of this analysis were:

- To process and analyze the historical trend of Mexico's per capita CO2 emissions from the World Bank.
- To apply the Box-Jenkins methodology to find the best-fitting time series model for the data.
- To evaluate the selected model's predictive accuracy on a hold-out test set.
- To generate forecasts through 2030 to assess the country's emissions trajectory.
- To interpret the forecasts in the context of Mexico's Nationally Determined Contribution (NDC) and SDG 13, providing data-driven strategic recommendations.

---

## 📈 Methodology & Key Findings

The analysis followed a rigorous statistical methodology:

1.  **Data Preparation:** The dataset was cleaned and transformed into a univariate time series from 1970 to 2019.
2.  **Stationarity Test:** An Augmented Dickey-Fuller (ADF) test concluded that the series is **stationary (d=0)**.
3.  **Model Identification:** A systematic search over various `ARIMA(p,0,q)` models was conducted. Based on the Akaike Information Criterion (AIC), the most parsimonious and best-fitting model was identified as an **Autoregressive model of order 1, or AR(1)**.
    - **Final Model:** `ARIMA(1,0,0)`
4.  **Model Diagnostics:** The residuals of the final model were analyzed and found to behave like white noise, with no significant autocorrelation remaining, as confirmed by diagnostic plots and the Ljung-Box test.
5.  **Forecasting & Conclusion:** The validated `AR(1)` model forecasts a **stabilization of per capita emissions around 3.8 tCO2e through 2030**. This flat trajectory is insufficient for meeting Mexico's climate goals.

---

## 📂 Repository Contents

- **`Forecasting_CO2_Mexico.ipynb`**: The main Jupyter Notebook containing the entire Python code, analysis, visualizations, and narrative for this project.
- **`CO2_emissions_mexico.csv`**: The raw data file sourced from the World Bank, used as the input for the analysis.
- **`Forecasting to Transform.pdf`**: The final project report, generated from the Jupyter Notebook.
- **`images/`**: A directory containing the plots and graphics used in the report and this README.
- **`README.md`**: This file, providing a summary of the project.

---

## 🛠️ Technologies Used

- **Python 3.9+**
- **Core Libraries:**
    - `pandas` & `numpy`: For data manipulation and numerical operations.
    - `statsmodels`: For statistical tests, time series models (ARIMA), and diagnostics.
    - `matplotlib`: For data visualization.
    - `scikit-learn`: For calculating model evaluation metrics (MAE, RMSE).

---

## 📊 Data Source

The data used in this project was sourced from **The World Bank**.
- **Indicator:** Carbon dioxide emissions (tCO2e per capita) excluding LULUCF
- **Series Code:** `EN.GHG.CO2.PC.CE.AR5`

---

## 👤 Author

- **Claudio Gonzalez**
    - **GitHub:** `https://github.com/ClaudioGlez21`