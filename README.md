# Customer Churn Prediction

## Project Overview
This project focuses on analyzing customer churn in a subscription-based business using machine learning models. The goal is to predict whether a customer will churn based on their demographic and subscription information.

## Dataset
The dataset used in this project is the `customer_churn.csv`, which contains various features related to customer demographics, subscription types, usage frequency, support calls, payment delays, and more. The target variable is `Churn`, indicating whether a customer has churned or not.

### Features:
- `Age`: Customer's age
- `Gender`: Customer's gender
- `Tenure`: Number of months the customer has been subscribed
- `Usage Frequency`: Frequency of usage of the service
- `Support Calls`: Number of calls made by the customer to support
- `Payment Delay`: Delay in payment
- `Subscription Type`: Type of subscription (e.g., Basic, Premium)
- `Contract Length`: Length of the contract (e.g., 1 year, 2 years)
- `Total Spend`: Total amount spent by the customer
- `Last Interaction`: Time of the last interaction with the customer
- `Churn`: Target variable (1 if churned, 0 if not)

## EDA (Exploratory Data Analysis)
We performed univariate and bivariate analysis to understand the distribution of the features and their relationships with the target variable, `Churn`.

### Univariate Analysis:
- Histograms and density plots were created for continuous variables such as `Age`, `Tenure`, `Usage Frequency`, and `Total Spend`.
- Bar plots were used for categorical variables like `Gender`, `Support Calls`, `Payment Delay`, `Subscription Type`, and `Contract Length`.

### Bivariate Analysis:
- We analyzed the relationship between `Age`, `Tenure`, `Subscription Type`, `Contract Length`, and `Churn` using histograms and count plots.
- We visualized how different features are distributed across the churn classes.

### EDA Insights:
- **Age**, **Tenure**, and **Usage Frequency** have no significant outliers.
- **Payment Delay** and **Subscription Types** show strong patterns correlated with churn.

## Preprocessing
- Handled missing values by dropping rows with `NaN` values.
- Encoded categorical variables using one-hot encoding for `Subscription Type` and ordinal encoding for `Contract Length`.
- Scaled numerical features using Min-Max Scaling.

## Model Training
We used three machine learning models to predict customer churn:
1. **Decision Tree Classifier**
2. **Logistic Regression**
3. **Random Forest Classifier**

The models were evaluated using accuracy, confusion matrix, and classification report.

### Model Performance:

#### Decision Tree:
- Accuracy: `{0.7659448300096635}`
- Confusion Matrix and Classification Report are provided.

#### Logistic Regression:
- Accuracy: `{0.840090485812176}`
- Confusion Matrix and Classification Report are provided.

#### Random Forest:
- Accuracy: `{0.8565184924887991}`
- Confusion Matrix and Classification Report are provided.

#### Grid Search Optimized Decision Tree:
- Accuracy: `{0.8532241061231661}`

## Hyperparameter Tuning
We used `GridSearchCV` to find the best hyperparameters for the Decision Tree model, improving its performance. The hyperparameters tuned included `max_depth`, `min_samples_split`, `min_samples_leaf`, and `criterion`.

## Model Interpretation
We visualized the decision tree using `plot_tree` to understand the decision-making process of the model.

## Installation Instructions
To run the project locally, follow the steps below:

## Requirements
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- warnings

## Future Work
- Advanced Models: Include advanced machine learning models like Gradient Boosting (XGBoost, LightGBM) and Neural Networks for potentially better performance.
- Class Imbalance: Address class imbalance using techniques like SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset and improve model predictions.
- Feature Selection: Perform feature selection techniques such as Recursive Feature Elimination (RFE) or SelectFromModel to optimize the model and reduce overfitting.
- Real-time Prediction API: Build a deployment-ready API (e.g., using Flask or FastAPI) for real-time churn prediction, allowing businesses to predict churn dynamically as new customer data arrives.

