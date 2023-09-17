# House-Price-Prediction
Models used : Linear Regression, Ridge Regression, Lasso Regression, Decision Tree, Random Forest and Gradient Boosting.

Approach Taken:

The provided code implements a machine learning pipeline to predict apartment prices based on various features. The pipeline involves data preprocessing, model training, and an interactive user interface for making predictions using different regression models. Here's an overview of the approach:

Data Preprocessing:

The code starts by reading a CSV file containing apartment data and loading it into a Pandas DataFrame.
The target variable "Price" is defined, and the features to be used for prediction are selected.
Missing values in the features are identified using a placeholder value (9) and replaced with NaN.
A SimpleImputer is used to fill missing values with the most frequent value in each column.

Model Selection and Training:

A dictionary of regression models (Linear, Ridge, Lasso, Decision Tree, Random Forest, Gradient Boosting) is defined.
For each model, it is trained on the preprocessed data (with imputed values) and evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).
The results are printed to compare the performance of different models.

Interactive User Interface:

The code uses the ipywidgets library to create an interactive user interface where users can input various feature values and select a model.
The make_prediction function takes user inputs, creates a DataFrame, replaces placeholder values with NaN, imputes missing values, and then predicts the apartment price using the selected model.
The predicted price is displayed to the user.

Challenges Faced:

Data Preprocessing: Dealing with missing values is a common challenge in data preprocessing. The code handles it using a placeholder value and imputation, but this approach might not always capture the true underlying patterns.

Model Evaluation: While evaluating models using training data is informative, it's crucial to assess their performance on unseen data (e.g., using cross-validation) to avoid overfitting.

Feature Selection: The choice of features used for prediction is essential. Including irrelevant or redundant features can lead to poor model performance.

Interactivity: Creating interactive interfaces requires careful consideration of user inputs, widget layout, and proper function integration.

Results Obtained:

The provided code demonstrates the training and evaluation of different regression models for predicting apartment prices. By comparing MAE, MSE, and RMSE metrics, we can observe the relative performance of these models on the given dataset.

Further, the predicted price of the house is displayed.

Improvement Opportunities:

Feature Engineering: Consider exploring additional feature engineering techniques to potentially improve model performance. Location parameters had been dropped & couldn’t be handled correctly as there were so many locations for different cities.

Cross-Validation: Evaluate models using cross-validation to obtain a more realistic estimate of their performance on unseen data.

Ensemble Methods: Explore ensemble methods that combine multiple models to potentially enhance predictive accuracy.
