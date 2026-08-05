# Building Energy Consumption Prediction ⚡🏢

This project is an end-to-end machine learning pipeline designed to predict the energy consumption of a building based on various environmental and operational factors. 

## 📊 Overview
Predicting energy usage accurately is critical for optimizing HVAC systems, reducing costs, and minimizing environmental impact. This project takes raw building data, cleans and preprocesses it, and applies machine learning to find the underlying patterns in energy consumption.

After experimenting with multiple algorithms (including Random Forest and XGBoost), a **Linear Regression** model was selected as the optimal choice, proving that simpler models often perform best when the underlying data patterns are highly linear.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** `pandas`
* **Machine Learning:** `scikit-learn` (StandardScaler, LinearRegression, Pipelines)
* **Visualization:** `matplotlib`

## 📈 The Dataset
The model is trained on a dataset containing 1,000 hourly records with the following features:
* **Numerical:** Temperature, Humidity, Square Footage, Occupancy, Renewable Energy, Hour of Day (Extracted from Timestamp).
* **Categorical:** HVAC Usage (On/Off), Lighting Usage (On/Off), Day of Week, Holiday status.
* **Target Variable:** EnergyConsumption

## 🚀 Key Steps & Workflow
1. **Exploratory Data Analysis (EDA):** Checked for missing values and visualized the relationships between individual features and total energy consumption using scatter plots.
2. **Feature Engineering:** Extracted the "Hour" from the raw Timestamp string to capture time-of-day usage patterns.
3. **Data Preprocessing:** Handled categorical variables using One-Hot Encoding (`pd.get_dummies()`).
4. **Pipeline Construction:** Built a robust `scikit-learn` pipeline incorporating a `StandardScaler` to normalize the data before passing it to the regression model, preventing data leakage.
5. **Model Evaluation:** Evaluated the model using Root Mean Squared Error (RMSE) and R-squared ($R^2$) metrics. 

## 🏆 Results
The Linear Regression model achieved the following performance on unseen test data:
* **R-squared ($R^2$):** ~0.59
* **RMSE:** ~5.15

**Overfitting Check:** The model achieved an $R^2$ of ~0.62 on the training data and ~0.59 on the testing data. Because these scores are so close, we can confidently conclude the model generalized well and did not overfit!

## 👤 Author
**Banoth Santhosh**
