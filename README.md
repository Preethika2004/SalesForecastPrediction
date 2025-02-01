# SalesForecastPrediction

## Introduction
This project focuses on predicting sales using historical sales data. The dataset includes various features such as date, sales, holiday indicators, past sales, previous year sales, and derived features like day of the week, day, month, year, and season. The goal is to build a predictive model that can forecast future sales based on these features. I have the data for 2021 to 2024. I used 2021 to 2023 data as train data, and 2024 data as test data.

## Table of Contents
- [Introduction](#Introduction)
- [Dataset](#Dataset)
- [Data Preprocessing & Feature Selelction](#Data-Preprocessing-&-Feature-Selelction)
- [Model Building](#Model-Building)
- [Results](#Results)

## Dataset
The dataset used in this project is stored in a CSV file named `sales_data.csv`. It contains the following columns:

- `date`: The date of the sales record.
- `sales`: The sales amount for that date.
- `holiday`: A binary indicator (0 or 1) indicating whether the date was a holiday.
- `past_sales`: The sales amount from the previous day.
- `previous_year_sales`: The sales amount from the same date in the previous year.

The following features are derived using the features we have in the dataset.
  
- `season`: A categorical variable indicating the season (0: winter, 1: spring, 2: summer).
- `day_of_week`: The day of the week (0: Monday, 6: Sunday).
- `day`: The day of the month.
- `month`: The month of the year.
- `year`: The year of the sales record.

## Data Preprocessing & Feature Selelction
The dataset undergoes several preprocessing steps to prepare it for modeling:

- `Loading the Dataset`: The dataset is loaded using pandas.
- `Date Conversion`: The date column is converted to a datetime object.
- `Feature Extraction`: Additional features such as day_of_week, day, month, year, and season are extracted from the date column.
- `Data Exploration`: Basic exploratory data analysis (EDA) is performed to understand the distribution of sales, holidays, past sales, and previous year sales.

## Model Building

The project uses a linear regression model to predict sales. The following steps are involved in building the model:

- `Feature Selection`: Relevant features are selected for the model. The features used include holiday, past_sales, previous_year_sales, season, - day_of_week, day, month, and year.
- `Train-Test Split`: The dataset is split into training and testing sets. Years 2021 to 2023 as train dataset, year 2024 as test dataset.
- `Model Training`: A linear regression model is trained on the training data. Linear regression is a simple yet powerful model that assumes a linear ---relationship between the input features and the target variable (sales).
- `Model Evaluation`: The model's performance is evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²).

## Results

The performance of the linear regression model is evaluated using the following metrics:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between predicted and actual sales. A lower MAE indicates better performance.
- **Mean Squared Error (MSE):** Measures the average squared difference between predicted and actual sales. MSE is more sensitive to large errors.
- **R-squared (R²):** Indicates the proportion of variance in the dependent variable that is predictable from the independent variables. An R² value closer to 1 indicates a better fit.

This is how our model is perrforming:
- `Mean Absolute Error (MAE):` 9.2200
- `Mean Squared Error (MSE):` 134.3288
- `R-squared (R²):` 0.5633
- **`Accuracy of the Model:`** 93.48%
