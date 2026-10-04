# House Price Prediction - Model Development Report

## 1. Project Overview

The objective of this project is to build a machine learning model that predicts house prices based on available property features.

The project compares multiple regression algorithms and evaluates their performance using MAE, MSE, RMSE and R² Score.

## 2. Dataset

Dataset: `house_prices.csv`

The dataset contains house/property information and the target variable `Price`.

The dataset was loaded using Pandas and checked for:
- Missing values
- Duplicate records
- Data types
- Basic statistical information

## 3. Data Preparation

The following preprocessing steps were performed:

- Property ID was excluded because it is an identifier rather than a predictive feature.
- Missing numerical values were handled using median imputation.
- Missing categorical values were handled using the most frequent value.
- Categorical variables were converted using One-Hot Encoding.
- Numerical features were standardized.
- The dataset was divided into training and testing sets using an 80:20 split.

## 4. Machine Learning Models

The following models were implemented and compared:

1. Linear Regression
2. Linear Regression from Scratch
3. Polynomial Regression
4. Decision Tree Regressor
5. Random Forest Regressor

## 5. Evaluation Metrics

Three required evaluation metrics were used:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score

RMSE was also calculated to provide an additional measure of prediction error.

## 6. Model Performance

| Model | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Random Forest | 1,472,445 | 3.974e12 | 1,993,538 | 0.9721 |
| Linear Regression | 2,188,736 | 8.454e12 | 2,907,633 | 0.9406 |
| Decision Tree | 2,491,788 | 9.603e12 | 3,098,882 | 0.9326 |
| Polynomial Regression | 2,367,902 | 1.012e13 | 3,180,590 | 0.9290 |

## 7. Best Model

The Random Forest Regressor achieved the best performance.

- MAE: 1,472,445
- MSE: 3.974e12
- RMSE: 1,993,538
- R² Score: 0.9721

The R² score of approximately 0.9721 means that the model explains about 97.21% of the variation in house prices on the test data.

Random Forest performed better than Linear Regression, Decision Tree and Polynomial Regression on the test dataset.

## 8. Cross-Validation

Five-fold cross-validation was performed on the Linear Regression model to check how consistently the model performs across different data splits.

The cross-validation results were generated in the notebook.

## 9. Predictions vs Actual Values

The project generates a visualization comparing actual house prices with predicted house prices.

Required output:

`predictions_vs_actual.png`

Points closer to the diagonal reference line indicate more accurate predictions.

## 10. Model Interpretation

The project also examines Linear Regression coefficients to understand the influence of transformed features on predicted house prices.

Feature interpretation results are available in the executed notebook.

## 11. Key Insights

1. Random Forest produced the highest R² score among the tested models.
2. Random Forest also produced the lowest MAE.
3. The Random Forest model achieved an R² score of approximately 97.21%.
4. Linear Regression also performed strongly with an R² score of approximately 94.06%.
5. Polynomial Regression did not improve performance over the simpler Linear Regression model.
6. The Decision Tree performed better than Polynomial Regression but worse than Random Forest and Linear Regression.
7. The actual-vs-predicted visualization provides a visual assessment of prediction quality.

## 12. Testing and Validation

The model was evaluated using a separate test dataset that was not used during model training.

Multiple regression algorithms were compared using standardized evaluation metrics.

This reduces the risk of selecting a model based only on a single metric.

## 13. Limitations

- The dataset size may limit how well the model generalizes to unseen real-world houses.
- Model performance depends on the available features.
- Additional feature engineering may improve predictions.
- Hyperparameter tuning could potentially improve Random Forest performance further.

## 14. Conclusion

The House Price Prediction project successfully demonstrates a complete beginner-level machine learning workflow.

The Random Forest Regressor was the best-performing model among the tested algorithms, achieving an R² score of approximately 0.9721.

The project demonstrates data preprocessing, train-test splitting, regression modelling, model evaluation, cross-validation and visualization of predictions.