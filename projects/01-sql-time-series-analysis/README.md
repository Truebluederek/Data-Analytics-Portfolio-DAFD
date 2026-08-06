# SQL + Python Time Series Analysis

A full pipeline analyzing retail sales data — from raw CSV to database to statistical decomposition — using SQL, SQLAlchemy, pandas, and matplotlib.

## What This Project Demonstrates

- **SQL querying**: date-range filtering (`BETWEEN`), aggregation (`GROUP BY`), and filtering on aggregated results (`HAVING`)
- **Database integration**: loading a CSV dataset into MySQL and querying it through Python using SQLAlchemy
- **Data cleaning**: type conversion (string → datetime), missing value checks
- **Time series analysis**: resampling to weekly frequency, linear interpolation for missing values, and STL (Seasonal-Trend decomposition using Loess) to separate trend, seasonality, and noise
- **Data visualization**: time series plots, multi-category trend comparison, and seasonal decomposition plots using matplotlib

## Dataset

`sales_data.csv` — 200 daily retail transactions (January–July 2024) across 5 products and 4 store locations, including transaction date, product ID, quantity sold, total sales, and store location.

## Key Findings

- Overall sales showed a **declining trend** across the analyzed period, isolated from day-to-day noise using STL decomposition.
- A **recurring weekly seasonal pattern** was identified — a signal that would be invisible in the raw daily data alone.
- One product (Product 104) stood out as both the highest-performing and most volatile week over week, suggesting closer inventory monitoring may be warranted.

## Tools Used

`Python` · `pandas` · `SQLAlchemy` · `MySQL` · `statsmodels` · `matplotlib` · `Jupyter Notebook`

## Files

- `notebook.ipynb` — full analysis, from database setup through visualization
- `sales_data.csv` — source dataset
