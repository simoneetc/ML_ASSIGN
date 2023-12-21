# ML_ASSIGN

# Housing Dataset Analysis

## Dataset Description
- [California Housing dataset](https://link-to-your-dataset) with 10 attributes: longitude, latitude, housing_median_age, total_rooms, total_bedrooms, population, households, median_income, median_house_value, ocean_proximity.
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
