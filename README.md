# Avocado Prices Prediction Analysis

## Background Context
- Avocados seem to be increasingly popular among millennials. It was observed that over 2.6 billion pounds of avocado were consumed in the United States alone in 2020, as opposed to only 436 million pounds consumed in the year 1985, as per Statista.
- Avocados are seen as a healthy option and are popular for being a good source of “good fats”. The fruit can be spread on toast, eaten raw, or even consumed in the form of a shake. Guacamole, which is a Mexican dip, is also made from avocados.
- Like most other products, the price of avocados fluctuates based on season and supply, which is why it would be beneficial to have a machine learning model to monitor and predict avocado prices.

## Problem Statement
- More awareness of the sales and prices of avocados can benefit the vendors, producers, associations, and companies. Price prediction based on sales would be a good input in the market to determine shifting of produce to locations where the fruit is more in demand or even encouragement of consumption in places where demand is not up to the mark.
- Due to the uncertainty in the prices, the companies are not able to sell their produce at the optimal price.
- This notebook provides a detailed analysis of historical avocado prices and sales volume across multiple US markets. The analysis focuses on identifying trends, seasonal patterns, regional variations, and relationships between price and volume using advanced statistical visualization techniques.
- The idea here is to predict future prices based on data collected of past prices based on geographical location, weather changes, and seasonal availability of avocados.

## Dataset
- The dataset represents weekly retail scan data for National retail volume (units) and price. Retail scan data comes directly from retailers’ cash registers based on actual retail sales of Hass avocados.
- The Average Price (of avocados) in the data reflects a per unit (per avocado) cost, even when multiple units (avocados) are sold in bags. The Product Lookup codes (PLU’s) in the data are only for Hass avocados. Other varieties of avocados (e.g. greenskins) are not included in this table.
- The dataset consists of the information about HASS Avocado. Historical data on avocado prices and sales volume in multiple US markets. Various variables present in the dataset includes Date, AveragePrice,Total Volume, Total Bags,Year,Type etc.
- The dataset comprises of 18249 observations of 14 columns.

## Implementing and Evaluating Models
- We are going to use the below models:

- Linear Regression: A fundamental machine learning algorithm used to model the relationship between a dependent variable and one or more independent variables.
- Random Forest Regression: An ensemble method that can capture complex relationships and interactions between features.
- Gradient Boosting Regression: A boosting algorithm that builds strong predictive models by combining the predictions of several base estimators.
- Extra Trees Regressor model: An ensemble learning method used for regression and classification tasks. It builds upon the principles of decision trees and random forests but introduces extra randomness to improve generalization and reduce overfitting.

- We are going to use the below matrices:
- MAE
- MSE
- RMSE
- R2

## Conclusion

- Among the four models tested — Linear Regression, Random Forest, Gradient Boosting, and Extra Trees Regressor — the Extra Trees Regressor delivered the best  -performance
- Random Forest also performed very well, closely trailing Extra Trees.
- Linear Regression showed the weakest performance, indicating that the relationship between features and avocado prices is non-linear and better captured by ensemble methods.
- Visual comparisons of predicted vs actual prices confirmed that Extra Trees and Random Forest models had predictions closely aligned with actual values.

## Recommendations

- Use Extra Trees Regressor for future avocado price predictions due to its superior accuracy and robustness.
- Feature Engineering: Consider adding more time-based features (e.g., week of year, holidays) or external factors (e.g., weather, economic indicators) to improve model performance.
- Model Deployment: Package the Extra Trees model into a pipeline for real-time or batch prediction in production environments.
- Monitoring: Regularly retrain the model with fresh data to maintain accuracy over time

## Future Work

- Hyperparameter Tuning: Use grid search or randomized search to fine-tune model parameters for even better performance.
- Cross-Validation: Implement k-fold cross-validation to ensure model stability and generalization.
- Regional Modeling: Build separate models for high-volume regions to capture localized pricing dynamics.
