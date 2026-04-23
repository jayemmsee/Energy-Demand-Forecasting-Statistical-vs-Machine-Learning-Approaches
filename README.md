# Energy-Demand-Forecasting-Statistical-vs-Machine-Learning-Approaches
Accurate forecasting of energy demand is critical for efficient resource allocation, cost optimization, and grid stability.

This project aims to predict short-term energy consumption using historical time series data and compare the performance of statistical and machine learning models.

**Tools & Technologies**
Python (pandas, NumPy, matplotlib)
statsmodels (SARIMA)
scikit-learn (Random Forest)
Jupyter Notebook

**Dataset**
Source: Kaggle – PJM Hourly Energy Consumption
Frequency: Hourly
Target Variable: Energy consumption (MW)

**Approach**
Data Preprocessing
Converted timestamp index to datetime format
Sorted data chronologically
Handled duplicate timestamps via aggregation
Ensured consistent hourly frequency
Performed missing value interpolation

**Exploratory Data Analysis**
Identified strong daily and weekly seasonality
Detected a potential structural break around 2013
Observed recurring consumption peaks linked to time-based patterns

**Statistical Modeling (SARIMA)**
Built SARIMA model to capture seasonal dependencies
Evaluated performance using MAE and RMSE
Observed good trend capture but limitations in peak prediction

**Machine Learning Modeling (Random Forest)**
Engineered time-based features:
Hour, day of week, month
Lag features (1 hour, 24 hours, 168 hours)
Trained Random Forest model on structured features
Evaluated using MAE and RMSE

**Results**
Model	MAE	RMSE
SARIMA	~3301	~3766
Random Forest	~312	~408

**Key Insights**
SARIMA effectively captured seasonal trends, but struggled with sharp fluctuations
Random Forest significantly outperformed SARIMA, particularly in capturing peak demand
Lag-based features proved highly effective for modeling temporal dependencies
The presence of a structural break highlights the importance of data stability in forecasting

**Business Impact**
Improved forecasting accuracy can enhance energy planning and cost efficiency
Better peak prediction supports grid reliability and demand management
Demonstrates the value of combining statistical and machine learning approaches

**Conclusion**
This project demonstrates that while traditional time series models are effective for capturing general patterns, machine learning models can provide superior performance in complex, real-world scenarios by leveraging feature engineering and non-linear relationships.
