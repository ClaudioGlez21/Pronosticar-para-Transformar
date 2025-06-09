# Forecasting for Transformation: A Time Series Analysis of Mexico's CO2 Emissions

![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)
![Libraries](https://img.shields.io/badge/libraries-pandas%2C%20statsmodels%2C%20matplotlib-orange)

## 📖 Overview

This project conducts a comprehensive time series analysis of Mexico's per capita CO2 emissions from 1970 to 2019. The primary goal is to apply the Box-Jenkins methodology to identify a robust forecasting model, project future emissions, and critically evaluate these forecasts in the context of Mexico's climate commitments under the Paris Agreement (its Nationally Determined Contribution, or NDC) and the UN's Sustainable Development Goal 13 (Climate Action).

The analysis reveals a high level of inertia in the emissions data and demonstrates that, without significant policy intervention, Mexico is not on track to meet its climate targets.

![Final Forecast Plot](images/final_forecast.png)
_**Note:** For the image above to display, create an `images` folder in your repository and save a screenshot of your final forecast plot as `final_forecast.png` inside it._

---

## 🎯 Project Objectives

- To process and analyze the historical time series of Mexico's per capita CO2 emissions from the World Bank.
- To test the series for stationarity using the Augmented Dickey-Fuller (ADF) test.
- To apply the Box-Jenkins methodology (using ACF/PACF plots and AIC) to identify and validate the most suitable ARIMA model.
- To evaluate the selected model's predictive accuracy on a hold-out test set using MAE, RMSE, and MAPE metrics.
- To generate forecasts through 2030 and interpret their implications for Mexico's climate policy and SDG 13.
- To provide data-driven strategic recommendations for policymakers.

---

## 📈 Methodology & Key Findings

The analysis followed a rigorous statistical methodology:

1.  **Data Preparation:** The dataset, sourced from the World Bank, was cleaned and transformed into a univariate time series from 1970 to 2019.
2.  **Stationarity Test:** An Augmented Dickey-Fuller (ADF) test was performed, which concluded that the series is **stationary (d=0)**.
3.  **Model Identification:** A systematic search over various `ARIMA(p,0,q)` (or `ARMA(p,q)`) models was conducted. Based on the Akaike Information Criterion (AIC), the most parsimonious and best-fitting model was identified as an **Autoregressive model of order 1, or AR(1)**.
    - **Final Model:** `ARIMA(1,0,0)`
4.  **Model Diagnostics:** The residuals of the final model were analyzed and found to behave like white noise, with no significant autocorrelation remaining (confirmed by diagnostic plots and the Ljung-Box test).
5.  **Forecasting & Conclusion:** The validated `AR(1)` model forecasts a **stabilization of per capita emissions around 3.8 tCO2e through 2030**. This flat trajectory reveals a significant **"implementation gap"** when compared to the steep decline required for Mexico to achieve its NDC target of a 35% emissions reduction. The core finding is that historical trends, if continued, are insufficient for meeting national climate goals.

---

## 🛠️ Technologies Used

- **Python 3.9+**
- **Core Libraries:**
    - `pandas`: For data manipulation and analysis.
    - `numpy`: For numerical operations.
    - `statsmodels`: For statistical tests, time series models (ARIMA), and diagnostics.
    - `matplotlib`: For data visualization.
    - `scikit-learn`: For calculating model evaluation metrics (MAE, RMSE).

---

## 🚀 How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
    cd YOUR_REPOSITORY_NAME
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    *(For best practice, you can create a `requirements.txt` file by running `pip freeze > requirements.txt` in your activated virtual environment).*
    ```bash
    pip install pandas numpy matplotlib statsmodels scikit-learn jupyterlab
    ```

4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter lab Forecasting_CO2_Mexico.ipynb
    ```
    You can then run the cells sequentially to reproduce the entire analysis.

---

## 📊 Data Source

The data used in this project was sourced from the **The World Bank**.
- **Indicator:** Carbon dioxide emissions (tCO2e per capita) excluding LULUCF
- **Series Code:** `EN.GHG.CO2.PC.CE.AR5`

---

## 👤 Author

- **Claudio Gonzalez**
    - **GitHub:** `[Your GitHub Profile URL]`
    - **LinkedIn:** `[Your LinkedIn Profile URL]`