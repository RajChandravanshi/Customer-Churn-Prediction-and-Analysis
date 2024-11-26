# Customer Churn Analysis and Prediction
This project focuses on analyzing customer churn using a dataset of customer activity and demographics. The goal is to perform exploratory data analysis (EDA) and build predictive machine learning models to classify churn outcomes. Hyperparameter tuning has been implemented to optimize model performance.

## Project Structure
1. Data Import and Cleaning
 - Loaded the dataset (customer_churn.csv) using Pandas.
 - Removed irrelevant columns (e.g., CustomerID).
 - Handled missing values and checked for duplicates.
 - Cleaned and preprocessed the dataset.

## 2. Exploratory Data Analysis (EDA)
- *Conducted univariate analysis for key features:
- Age, Tenure, Usage Frequency, Support Calls, Payment Delay, Subscription Type, Contract Length, and Total Spend.
- Visualized data distributions using histograms, KDE plots, and boxplots.
- Checked for skewness and outliers.
*- Conducted bivariate analysis:*
- Analyzed relationships between features and churn using count plots, histograms, and correlation heatmaps.
- Explored categorical variables like subscription type and contract length against churn.
