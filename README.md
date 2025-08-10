📌 Overview
This project is a machine learning–based forecasting model designed to predict future power generation for a specific turbine at a specific NHPC dam. Using time-series data collected at 15-minute intervals over several years, the model leverages advanced algorithms like XGBoost, LightGBM, and CatBoost (with hyperparameter tuning via Optuna) to produce accurate long-term predictions.

The primary goal is to assist dam operators and planners in optimizing operations, planning maintenance, and ensuring reliable power supply by providing accurate forecasts of power output under varying conditions.

🎯 Why This Project Was Needed
Power generation at hydroelectric dams depends on a variety of dynamic factors such as water flow, turbine efficiency, and weather conditions. For organizations like NHPC (National Hydroelectric Power Corporation), predicting future output is crucial for:

Grid Stability → Helps balance supply and demand in the power grid.

Maintenance Scheduling → Allows operators to plan turbine servicing during low-output periods.

Operational Efficiency → Improves water resource management and turbine usage strategies.

Financial Planning → Assists in revenue forecasting and bidding in power markets.

Renewable Energy Integration → Supports grid operators in managing variability from hydro sources alongside other renewables like wind and solar.

Without accurate forecasting, operators risk overproduction (leading to wastage) or underproduction (causing shortages and instability in the power grid). Our model bridges this gap by using historical and environmental data to provide data-driven, actionable predictions.

🛠️ Features
Long-term forecasting (days to years ahead)

Support for multiple dams and turbines

Inclusion of weather and lag features for improved accuracy

Advanced stacking ensemble with Optuna tuning

Visualization of trends, forecasts, and model performance

📊 Tech Stack
Python (Pandas, NumPy, Scikit-learn, Optuna)

XGBoost, LightGBM, CatBoost (Ensemble Learning)

Matplotlib, Plotly, Seaborn (Data Visualization)

Jupyter Notebook (Development Environment)


📈 Results
Achieved high forecasting accuracy with a hybrid stacking approach.

Demonstrated reliable performance on multi-year datasets.

Provided interpretable feature importance plots for operational insights.
