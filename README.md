# Sales Forecasting and Inventory Optimization

## Project Overview
This project applies predictive analytics and machine learning techniques to forecast daily sales and optimize inventory management across multiple stores and products. The goal is to minimize stockouts, optimize stock levels, and provide insights for data-driven promotional strategies.

## Key Features
- **Sales Forecasting**: Predicts daily sales for each product at different stores using historical data.
- **Inventory Optimization**: Recommends optimal stock levels based on predicted sales.
- **Promotion Strategy**: Identifies products suitable for promotion based on sales trends and inventory levels.

## Data
The dataset includes:
- **Store ID** and **Product ID**
- **Daily Sales** (`quantity_sold`)
- **Revenue per product**
- **Date Information** (day of the week and month)

## Approach
1. **Data Preprocessing**: Cleaned the data and created new features such as day of the week and month.
2. **Feature Engineering**: Added features like `RevenuePerDayOfWeek` and `RevenuePerMonth` to improve model accuracy.
3. **Model Selection**: Applied and tuned multiple models using cross-validation, including Linear Regression, Random Forest, and K-Nearest Neighbors.
4. **Sales Forecasting**: Predicted sales for the first week of July 2024.
5. **Inventory Recommendations**: Provided optimal stock levels to meet predicted demand.

## Models and Results
- **Linear Regression**: Baseline model with RMSE of 63,115.35.
- **Random Forest Regressor**: Best-performing model with an RMSE of 1.22, tuned with hyperparameters: `max_depth=10`, `min_samples_split=10`, `n_estimators=500`.
- **K-Nearest Neighbors**: RMSE of 1.30 with optimal parameters: `n_neighbors=10`, `weights=uniform`, `metric=manhattan`.

## Results
Here are sample inventory recommendations based on the predicted sales:

| Store ID | Product ID | Recommended Quantity Sold |
|----------|------------|---------------------------|
| 1        | 1          | 43.82                     |
| 1        | 2          | 45.57                     |
| 1        | 3          | 51.68                     |
| ...      | ...        | ...                       |
| 3        | 105        | 34.63                     |
| 3        | 106        | 53.99                     |
