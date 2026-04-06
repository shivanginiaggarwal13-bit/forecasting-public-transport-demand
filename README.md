# forecasting-public-transport-demand
Time-series forecasting of passenger arrivals using STL+SARIMA, ETS, and Regression 

## Business Problem
A public transportation company needs reliable demand forecasts
to plan bus acquisitions and terminal expansion. Using 3 weeks
of historical 15-minute passenger arrival data, I built and
compared multiple forecasting models.

## Dataset
- Source: BICUP 2006 Competition Dataset
- 1,302 records across 21 days (March 2005)
- 15-minute intervals from 6:30–22:00
- Train: March 1–14 | Test: March 15–21

## Approach
1. **EDA** — Identified daily seasonality, weekday vs weekend
   patterns, zero-demand periods
2. **Models Built:**
   - Seasonal Naive (baseline)
   - STL Decomposition + SARIMA
   - Exponential Smoothing (ETS)
   - Linear Regression with time features
3. **Evaluation** — RMSE, MAE, MAPE on both train and test data

## Key Results
| Model | Test MAE | Test MAPE |
|---|---|---|
| Seasonal Naive | 21.91 | 501.82 |
| STL + SARIMA | 19.81 | 355.36 |
| ETS | 20.07 | 203.86 |
| Linear Regression | 12.55 | 167.06 |

**Best model: Linear Regression** — most generalizable,
captures hour-of-day and weekend patterns effectively.

## Tools & Libraries
Python | Pandas | NumPy | Statsmodels | Scikit-learn | Matplotlib

## Author
**Shivangini Aggarwal**
Data Analyst | ISB AMPBA Co'26
[LinkedIn](https://linkedin.com/in/shivangini-aggarwal)
