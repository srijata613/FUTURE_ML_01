Retail Sales Forecasting Project (Superstore Data)

Predictive Analytics Internship Project — Time Series Forecasting for Retail

🧠 Project Overview

This project uses historical sales data from a “Superstore” to build a time‐series forecasting model (using Facebook Prophet) and presents the results through an interactive dashboard (built in Power BI).
The objective: forecast the next 12 months of total sales, enabling stakeholders to optimise inventory planning, staffing, and marketing spend.

📌 Key Business Outcomes & Findings

* Generated a 12-month forecast of total sales based on 4 years of historical data.
* Predicted a ~6.3% year-on-year growth in revenue.
* Identified peak sales season in November/December (≈150% above average) and highest daily sales volume on Fridays/Mondays.
* Actionable insights:

  * Increase stock procurement by ~150% beginning October to manage Q4 surge.
  * Align staffing to the high-volume days (Friday/Monday) and reduce coverage during slower days/weeks.
  * Launch marketing push in Jan/Feb to mitigate the post‐holiday trough.

🛠 Methodology & Technical Stack

| Stage                | Framework / Tool | Description                                                                                |
| -------------------- | ---------------- | ------------------------------------------------------------------------------------------ |
| Data Preparation     | Python (pandas)  | Aggregated transactional data into a daily time-series (`ds`, `y`); handled missing dates. |
| Feature Engineering  | Python (Prophet) | Created custom holiday dataframe; modelled yearly & weekly seasonality.                    |
| Modelling            | Facebook Prophet | Trained on 4 years of data; generated ~365-day forecast.                                   |
| Dashboard & Analysis | Power BI (DAX)   | Built interactive dashboard showing actual vs predicted, drill-down by month/day.          |

📁 Repository Structure

```
CODE/
  ├─ sales_forecasting_colab.py        # Main Python script for data prep, modelling & forecasting  
  ├─ requirements.txt                   # Python dependencies  
DATA/
  ├─ (raw + processed datasets)  
OUTPUT/
  ├─ forecast_results.csv               # Forecast output  
VISUALIZATION/
  ├─ Power BI dashboard files (.pbix)   # Interactive dashboard  
.gitignore  
LICENSE  
README.md
```

🔍 How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/srijata613/FUTURE_ML_01.git  
   ```
2. Navigate into the `CODE` directory and install dependencies:

   ```bash
   cd FUTURE_ML_01/CODE  
   pip install -r requirements.txt  
   ```
3. Open `sales_forecasting_colab.py` and run the notebook/script (either locally or in Google Colab).
4. After forecasting is complete, open the Power BI dashboard in `VISUALIZATION/` to explore results.
5. Review the `OUTPUT/forecast_results.csv` for tabular results or export visualisations as needed.

✅ Key Results & Screenshots

* The central chart on the dashboard shows historical sales (solid line) transitioning into the forecasted future (dashed line).
* Additional visuals: Sales by month (highlights Q4 spike), Sales by day of week (shows Monday/Friday peaks).
* These insights informed the recommendations around inventory, staffing and marketing.

📈 Next Steps & Enhancements

* *Segmented Forecasting*: Extend the model to forecast by region or product-category (e.g., Furniture vs Technology) for more granular insights.
* *Model Validation*: Add residual plots, cross-validation (time-series folds) and compute metrics like MAE, RMSE to enhance robustness.
* *Automated Pipeline*: Prepare the codebase for automated/batch forecasting (e.g., monthly updates) and integrate with visualization refresh.
* *Feature Expansion*: Incorporate additional exogenous variables (promotions, holidays, price changes) to boost predictive power.

## 📋 Dependencies

A full list of Python libraries is in `CODE/requirements.txt`. At minimum you’ll need:

* `pandas`, `numpy` – for data manipulation
* `fbprophet` (or `prophet`) – for time-series forecasting
* `matplotlib`, `seaborn` – for plots (if used)
* `Power BI` desktop – to view the dashboard (free version works)

## 📝 License

This project is licensed under the terms specified in the `LICENSE` file.
