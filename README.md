# ML_ASSIGN

# Housing Dataset Analysis

## Dataset Description
- [California Housing dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html) with 10 attributes: longitude, latitude, housing_median_age, total_rooms, total_bedrooms, population, households, median_income, median_house_value, ocean_proximity.
- 20,641 readings with varied records for each class of ocean_proximity.

## Methodology
- Ensembling techniques: Bagging and Random Forest.

## Pipeline Explanation
- **Feature Selection:** Uses `SelectFromModel` with a `RandomForestRegressor` as the estimator to select important features.
- **Scaling:** Applies `StandardScaler` to standardize the features.
- **Regressor:** Utilizes `RandomForestRegressor` for the final prediction.

## GridSearchCV
- **Approach:** Exhaustively searches through a predefined set of hyperparameter values.
- **Method:** Evaluates the model's performance for every possible combination of hyperparameter values specified in a grid.
- **Pros:** Guarantees finding the best combination if it exists within the specified grid.
- **Cons:** Can be computationally expensive, especially when the hyperparameter space is large.

## RandomizedSearchCV
- **Approach:** Randomly samples hyperparameter values from a distribution over a fixed number of iterations.
- **Method:** Evaluates the model's performance for a random subset of hyperparameter combinations.
- **Pros:** More efficient for large hyperparameter spaces, as it doesn't need to explore all possibilities.
- **Cons:** It might not find the optimal combination, but it can often discover good configurations more quickly.

## Conclusion
- RandomizedSearchCV is a more efficient alternative to GridSearchCV, particularly in scenarios where the hyperparameter space is large, and an exhaustive search becomes impractical.
  _______________________________________________________________________________________________________________________________________________________________________________________________________________

  # Customer Churn Dataset

# Customer Churn Dataset

## Dataset Description
- [The Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) is available in .csv format and comprises 12 attributes: CustomerID, Age, Gender, Tenure, Usage, Frequency, Support, Calls, Payment, Delay, Subscription Type, Contract Length, Total Spend, Last Interaction, and Churn.



## Methodology
- The dataset captures the rate at which customers discontinue a company's products or services within a specified timeframe. Churn is a pivotal metric impacting revenue, growth, and customer retention.

- In this dataset, the churn label distinguishes between customers who have discontinued (churned) and those who remain engaged (non-churned). Analyzing churn behavior allows companies to develop strategies for customer retention, enhance satisfaction, and reduce turnover. Predictive modeling techniques can forecast and proactively address potential churn, enabling proactive measures to retain at-risk customers.

- The notebook's goal is to gain insights through customer segmentation using the k-means clustering algorithm and build a classification model to predict churn probability.

## Conclusion
Based on the analysis, the following conclusions are drawn:
1. Female customers are more prone to churn than male customers.
2. Customers above the average age (40 years old) have a higher probability of churn.
3. Customers with short-term contracts (Monthly) tend to churn more than those with long-term contracts (Quarterly and Annual).
4. Customers making more than four support calls increase the probability of churn.
5. Customers with payment delays exceeding the sample average (12 months) are more likely to churn.
6. Customers with lower spending scores tend to churn more than those with higher spending scores.
7. Customers with up-to-date interactions tend to churn less.

**Note:** These insights can guide businesses in implementing targeted strategies to mitigate churn and improve overall customer satisfaction.
