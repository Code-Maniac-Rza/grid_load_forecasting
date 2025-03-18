# Grid Load Forecasting & Optimization

## Overview
This project focuses on forecasting electricity demand and optimizing grid load balancing using machine learning models. The objective is to accurately predict electricity demand using historical data and external factors like temperature, humidity, and renewable energy generation. The best-performing model is then used to optimize grid allocation to minimize load imbalance.

## Features
- **Electricity Demand Forecasting:** Predict future electricity consumption based on historical data.
- **Weather Data Integration:** Fetches temperature and humidity using OpenWeatherMap API.
- **Multiple Model Comparison:** Uses Random Forest and XGBoost for demand forecasting.
- **Grid Load Balancing:** Optimizes electricity allocation using `scipy.optimize.minimize`.
- **Visualization:** Plots actual vs. predicted demand and optimized allocation.

## Dataset
The dataset includes columns such as:
- `settlement_date`: Date of electricity usage.
- `settlement_period`: 30-minute intervals for each day.
- `england_wales_demand`: Actual electricity demand in England and Wales.
- `latitude`, `longitude`: Location coordinates (for weather data).
- `embedded_wind_generation`, `embedded_solar_generation`: Renewable energy production.
- `is_holiday`: Indicates if the day is a public holiday.

## Dependencies
Ensure you have the following Python libraries installed:
```bash
pip install pandas numpy requests matplotlib seaborn scikit-learn xgboost scipy
```

## Usage
1. **Prepare Data:** Load the dataset (`electricity_usage.csv`).
2. **Feature Engineering:** Extract time-related features and fetch weather data.
3. **Train Models:** Train and evaluate Random Forest, and XGBoost.
4. **Optimize Grid Load:** Apply optimization to balance electricity allocation.
5. **Visualize Results:** Generate plots comparing actual vs. predicted demand.

## Running the Project
Run the script using:
```bash
python grid_load_forecast.py
```

## Results
The script compares models based on Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE), selecting the best-performing model for grid optimization.
Random Forest - MAE: 633.7881080693963, RMSE: 953.8730555469846
XGBoost - MAE: 1107.5189570411112, RMSE: 1496.634714810128

<img width="758" alt="image" src="https://github.com/user-attachments/assets/5bfb6c7e-c258-46c0-8cec-40b9baf41c31" />


## Future Enhancements
- **Real-time Weather Data Integration**
- **Deep Learning Models for Improved Accuracy**
- **Scalability for Larger Datasets**

## Author
Shahryar Rza

