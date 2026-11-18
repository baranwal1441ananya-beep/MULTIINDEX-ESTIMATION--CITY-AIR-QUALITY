#Multi-City Air Quality Index (AQI) Estimation Using Machine Learning

# About the Project

This project uses machine learning regression techniques to estimate the daily Air Quality Index (AQI) of different Indian cities based on air pollutant measurements.

The project analyses historical air quality data and compares four regression algorithms to identify the model with the best predictive performance.

# Objectives

- Estimate daily AQI using pollutant measurements.
- Analyse air quality data across multiple Indian cities.
- Preprocess the dataset and handle missing values.
- Train and compare different regression models.
- Evaluate model performance using error metrics.

# Dataset

The project uses the `city_day.csv` dataset, containing daily air quality measurements from 26 Indian cities.

*Dataset details:
- Original records: 29,531
- Original columns: 16
- Cities covered: 26
- Time period: 2015–2020
- Target variable: AQI

*Features used:
- PM2.5
- PM10
- NO
- NO2
- NOx
- NH3
- CO
- SO2
- O3
- Benzene
- Toluene
- City
- Year, Month and Day

#Technologies & Libraries

- Python
- Pandas – Data manipulation
- NumPy – Numerical operations
- Matplotlib – Data visualization
- Seaborn – Statistical visualization
- Scikit-learn – Machine learning and evaluation

# Project Workflow

1. Data Loading – Imported the air quality dataset.
2. Data Cleaning – Removed the Xylene column and rows with missing AQI values.
3. Feature Engineering – Extracted Year, Month and Day from the Date column.
4. Data Preprocessing – Handled missing values, scaled numerical features and encoded categorical data.
5. Data Splitting – Used a chronological 80:20 train-test split.
6. Model Training – Trained four regression algorithms.
7. Model Evaluation – Compared predictions using MAE, MSE, RMSE and R² score.

# Machine Learning Models

The following regression algorithms were implemented:

1. Linear Regression
2. K-Nearest Neighbors (KNN) Regression
3. Decision Tree Regression
4. Random Forest Regression

# Model Performance

| Model | R² Score |
| Linear Regression | 0.8668 |
| KNN Regression | 0.7447 |
| Decision Tree | 0.7613 |
| Random Forest | **0.9060** |

#Best Model: Random Forest Regression

Random Forest achieved the best overall performance.

- **R² Score:** 0.9060
- **MAE:** 16.62
- **MSE:** 760.74
- **RMSE:** 27.58

The R² score indicates that the model explains approximately 90.6% of the variation in AQI values in the test dataset. It should not be interpreted as 90.6% accuracy.

## Feature Importance

The Random Forest model identified the following as its most influential features:

- PM2.5 – 47.31%
- CO – 37.68%
- NO – 3.68%
- PM10 – 3.50%

PM2.5 and CO together account for approximately 85% of the model's impurity-based feature importance.

## Results & Conclusion

Among the four regression models, Random Forest performed best based on the evaluation metrics.

The project demonstrates how machine learning can estimate daily AQI values using historical pollutant measurements. It also highlights differences in prediction errors across AQI ranges and cities.

Note:This project estimates same-day AQI from pollutant readings. It is not a future AQI forecasting system.



