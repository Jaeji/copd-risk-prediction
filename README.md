# COPD Mortality Analysis: Forecasting and Risk Classification

An applied data analysis project examining provincial COPD mortality patterns in Thailand using historical data from 2019–2023 (B.E. 2562–2566), with a 2024 (B.E. 2567) forecast and risk classification.

## Project Objectives

- Explore changes in COPD mortality rates over time and across health zones.
- Estimate the following year's mortality rate for each province.
- Group provinces into relative risk categories based on forecast values.
- Visualize geographic patterns in the results.

## Workflow

1. **Data Preparation** – Prepare province-level mortality data, exclude national and regional summary rows, and organize observations by province and year.
2. **Statistical Analysis** – Use one-way ANOVA to examine differences across years and health zones.
3. **Forecasting** – Fit a separate Linear Regression model for each province using its historical annual rates to estimate the next year's rate.
4. **Risk Classification** – Define Low, Medium, and High categories using quantiles of forecast values, then apply K-Nearest Neighbors (KNN) using geographic coordinates and forecast values.
5. **Visualization** – Present mortality trends and geographic risk patterns.

## Tools & Technologies

- Python
- pandas, NumPy
- SciPy
- scikit-learn
- Matplotlib
- Jupyter Notebook

## Repository Contents

- `copd_risk_prediction.ipynb` – Main analysis notebook.
- `requirements.txt` – Python package dependencies.
- `data/` – Directory for the source workbook (not included).

## How to Run

```bash
pip install -r requirements.txt
```

Place the source workbook expected by the notebook in the `data/` directory, then run `copd_risk_prediction.ipynb` from top to bottom.

## Notes

The regression models are fitted separately for each province using a limited historical time series. Forecasts and risk categories should therefore be interpreted as exploratory estimates rather than definitive public-health predictions.
