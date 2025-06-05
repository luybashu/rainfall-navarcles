# 🌧️ Rainfalls in Navarcles: Visualization and Forecasting

## Project Overview

This project explores 30 years of rainfall data in **Navarcles**, a municipality in Catalonia, Spain. It combines **time series forecasting** techniques with **interactive data visualization** to both analyze historical precipitation and predict future rainfall.

The project has two key goals:
1. **Forecast monthly rainfall** using time series models (SARIMA, SARIMAX, Prophet, Auto-ARIMA) and machine learning models (LightGBM, CatBoost, ElasticNet).
2. **Create a public dashboard** in Tableau to make precipitation trends accessible to residents and local authorities.

The best-performing model was **Auto-ARIMA**, achieving a test MAE of 29.19 mm.

The project is organized into the following folders:


## Key Features

- **Private rainfall dataset (1995–2024)** manually recorded in Navarcles.
- **Comparison of multiple forecasting models** including SARIMA, SARIMAX, Prophet, LightGBM, CatBoost, and ElasticNet.
- **External regressors** (temperature, insolation, lagged rainfall, etc.) explored for enhanced accuracy.
- **Interactive dashboard** developed with Tableau (Public Edition) for public engagement.
- **Python-based data pipeline**, including preprocessing, stationarity tests, ACF/PACF analysis, and time series cross-validation.

---

## Requirements

To run the Jupyter notebooks:

- Python 3.10+
- JupyterLab 4.2+
- Install dependencies from `requirements.txt`
  
```bash
pip install -r requirements.txt
```

## Repository Structure

<details>
<summary><strong>data/</strong> – Raw and processed data files</summary>

- `navarcles_private_data.csv` – Manually collected rainfall data (1995–2024)
- `manresa_meteorological_data.csv` – Public weather data from Manresa (temp, insolation, rainfall)
- `parsed_city_hall_data.csv` – Parsed rainfall data from City Hall web archive

</details>

<details>
<summary><strong>script/</strong> – Jupyter notebooks for analysis</summary>

- `1_EDA_and_Modeling.ipynb` – Full exploratory analysis, preprocessing, model training, evaluation, and forecasting
- `2_Data_Parsing_CityHall.ipynb` – Scraper and parser for public rainfall records (for Manresa/Navarcles)

</details>

<details>
<summary><strong>results/</strong> – Project deliverables</summary>

- `Final_Report_Rainfall_Navarcles.pdf` – Full project report (this document)
- `Dashboard_Navarcles.twbx` – Tableau dashboard file (open with Tableau Desktop Public Edition)
- `Presentation_Rainfall_Navarcles.pdf` – Summary slide deck for presentation

</details>
