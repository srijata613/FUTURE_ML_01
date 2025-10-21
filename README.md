# Retail Sales Forecasting Project (Superstore Data)
### Predictive Analytics Internship Project

This project uses historical Superstore sales data to develop and deploy a time-series forecasting model (Facebook Prophet) and visualize the results in an interactive Power BI dashboard.

Retail Sales Forecasting Project: Superstore Data

Predictive Analytics Internship Project: Time Series Forecasting for Retail

This project focuses on leveraging historical transactional data from the Superstore dataset to build a robust time series forecasting model using Facebook Prophet. The goal was to accurately predict the next 12 months of total sales, enabling the business to optimize inventory, staffing, and marketing spend.

🚀 1. Key Business Outcomes & Findings

The analysis successfully generated a 1-year sales forecast, providing the necessary data for strategic planning.

Metric

Historical Value (2014-2017)

Predicted Value (Next 12 Months)

Actionable Insight

Total Revenue

$\approx \$2.30 \text{ Million}$

$\approx \$615,000$

Predicted 6.3% YOY Growth for the coming year.

Peak Season

November / December

Confirmed Q4 surge (150% above average).

Inventory Alert: Must increase stock orders by 150%+ starting in October.

Operational Peak

Friday / Monday

Highest sales volume days.

Staffing Optimization: Schedule max coverage on these two days.

Actionable Recommendations

Inventory Management: Increase stock procurement and storage capacity by 150% starting in October to prevent stock-outs during the predictable Q4 peak season.

Staffing Efficiency: Reallocate labor hours to match demand patterns, ensuring maximum staffing levels on Fridays and Mondays and minimum essential coverage on the slower weekend/mid-week days.

Marketing Strategy: Launch a significant demand generation campaign in January/February to mitigate the severe post-holiday sales trough predicted by the model.

🛠️ 2. Methodology & Technical Stack

The project followed a standard data science pipeline, translating raw transactional data into a clean time series forecast.

Stage

Tool / Library

Key Task

Data Preparation

Python (Pandas)

Aggregated transactional data (Sales) to a daily time series (ds, y) and handled missing dates.

Feature Engineering

Python (Prophet)

Generated a custom holidays dataframe and incorporated yearly/weekly seasonality components.

Modeling

Facebook Prophet

Trained on 4 years of historical data to capture complex multiplicative seasonality and generate a 365-day continuous forecast (yhat).

Data Analysis

Power BI (DAX)

Created measures like Forecast Period Sales and Total Actual Sales to isolate and compare historical vs. predicted revenue.

Visualization

Power BI

Built a fully interactive dashboard to display the forecast and diagnostics.

Code References

The full data processing and modeling script is available in: CODE/sales_forecasting_colab.py

Python dependencies are listed in: CODE/requirements.txt

📊 3. Visual Results (Power BI Dashboard)

The final dashboard structure, simulated below, allows stakeholders to instantly grasp the overall trend (top chart) and drill down into operational specifics (bottom charts).

Dashboard Main View

The central chart shows the transition from observed sales (solid line) to the model's future prediction (dashed line), providing a continuous 4-year visual timeline.

Placeholder for Screenshot: 
![Dashboard_Main_View](https://github.com/user-attachments/assets/0ccbf848-7bd6-4131-8693-95f7f9e9a7e4)



Seasonal & Operational Insights

These charts provide the justification for the business recommendations, highlighting the peaks and troughs.

Sales by Month (Inventory Focus)

Sales by Day of Week (Staffing Focus)

Shows: Extreme seasonal spikes in Q4 (Nov/Dec) and the corresponding low demand in Q1 (Jan/Feb).

Shows: Consistent daily patterns, confirming that operational workload is heaviest on Mondays and Fridays.





💡 Next Steps for Future Iteration

Segmented Forecasting: Rerun the Prophet model to forecast sales by Region and by Product Category to provide granular insights for local managers and inventory planning for specific product lines (e.g., Furniture vs. Technology).

Model Validation: Introduce explicit residual plots and use cross-validation techniques (like those in Prophet) to formally quantify the model's mean absolute error (MAE) and bias, enhancing professional credibility.


