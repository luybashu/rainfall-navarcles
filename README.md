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

---

## Forecasting Summary

| Model          | Avg. MAE (CV) |
|----------------|---------------|
| **Auto-ARIMA** | **29.35**     |
| Prophet        | 29.72         |
| SARIMA         | 32.80         |
| SARIMAX        | 30.63         |
| LightGBM       | 30.98         |
| CatBoost       | ~31.12        |
| Constant Model | ~31.00        |

> Final test MAE of Auto-ARIMA: **29.19 mm**

---

## Dashboard Preview

The interactive Tableau dashboard includes:

- **Annual Analysis**:
  - Mean annual rainfall
  - Rainiest/driest years
  - Longest wet/dry periods

- **Monthly View**:
  - Number of rainy days
  - Monthly extremes and totals

- **Snowfall Tracking**:
  - Historical snow event logs

- **User Controls**:
  - Filter by year or month
  - Explore trends with dropdowns and charts

> Open `Dashboard_Navarcles.twbx` with **Tableau Desktop Public Edition (v2022.3+)**

---

## Methodology Summary

- **Data Preprocessing**:
  - Manual dataset cleaned and merged with Manresa data
  - Monthly aggregation and missing value imputation

- **Stationarity & Seasonality**:
  - ADF test, ACF/PACF, seasonal decomposition

- **Modeling Approaches**:
  - SARIMA, Auto-ARIMA, SARIMAX
  - Prophet, ElasticNet, LightGBM, CatBoost

- **Validation Strategy**:
  - Time-series cross-validation
  - Mean Absolute Error (MAE) as the evaluation metric

- **External Regressors Tested**:
  - Temperature, insolation, rainfall stats, lagged features

---

## Future Work

- [ ] Add reanalysis or satellite-based weather features
- [ ] Investigate deep learning models (e.g., LSTM, Temporal Fusion Transformer)
- [ ] Deploy dashboard online for public access
- [ ] Collaborate with local authorities for real-time data updates

---

## License

This project is intended for **educational and non-commercial use**.  
Please credit the author and repository if reusing parts of the methodology or data.
- `Presentation_Rainfall_Navarcles.pdf` – Summary slide deck for presentation

</details>
