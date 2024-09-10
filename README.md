### Project Title: Predicting the Number of Shares for Online News Articles

**Author:** Arunsingh K.  

---  

#### Executive Summary
This project focuses on predicting the number of shares an online news article will receive using various regression models. The RandomForest Regressor, after hyperparameter tuning, demonstrated the best performance with an R² of 0.9995 and a low MAE of 6.14. The project involved training multiple models, evaluating their performance, and fine-tuning the RandomForest model to enhance accuracy.

#### Rationale
Predicting the number of shares a news article will receive is valuable for media companies and content creators. It can guide content strategies, optimize marketing efforts, and improve user engagement by tailoring articles to audience preferences.

#### Research Question
How can we accurately predict the number of shares an online news article will receive before it gets published?

#### Data Sources
The analysis uses the Online News Popularity Dataset from the UCI Machine Learning Repository. This dataset includes features related to the content and publication of news articles, along with the number of shares each article received.  

It consists of 39,644 rows and 61 columns, summarizing features about articles published by Mashable over a two-year period. This dataset is ideal for practicing skills in exploratory data analysis, data visualization, and regression/classification modeling techniques.

#### Methodology
1. **Data Cleaning and Preprocessing**: Addressed missing values, encoded categorical variables, and split the dataset into training and test sets.
2. **Model Training and Evaluation**: Evaluated various regression models, including Dummy Regressor, Linear Regression, SVM Regressor, Decision Tree Regressor, RandomForest Regressor, and XGBoost.
3. **Hyperparameter Tuning**: Applied BayesSearchCV to optimize the RandomForest Regressor, finding the best parameters to enhance model performance.
4. **Model Comparison**: Compared models using metrics such as MAE, MSE, RMSE, R², and MAPE.

#### Results
- **Dummy Regressor**: High MAE of 2,899.46 and R² close to zero.
- **Linear Regression**: Perfect performance with an R² of 1.0, which is unusual and suggests potential overfitting.
- **SVM Regressor**: Poor performance with MAE of 2,115.43 and a negative R² value.
- **Decision Tree Regressor**: Good performance with MAE of 12.08 and high R² of 0.998546.
- **RandomForest Regressor**: Best performance with an MAE of 7.65, MSE of 38,232.89, RMSE of 195.53, and R² of 0.999251. After hyperparameter tuning, the metrics improved to MAE of 6.14, MSE of 24,927.94, and R² of 0.9995.
- **XGBoost**: Moderate performance with higher MAE and RMSE compared to RandomForest.

**Forecasted Details:**
The RandomForest Regressor was trained on the full training data and tested on the test set. The first few predictions were as follows:
- Actual Shares: 1200, Predicted Shares: 1200.0
- Actual Shares: 711, Predicted Shares: 711.0
- Actual Shares: 843, Predicted Shares: 843.0
- Actual Shares: 3400, Predicted Shares: 3400.0
- Actual Shares: 3400, Predicted Shares: 3400.0

Evaluation metrics for the RandomForest Regressor on test data:
- MAE: 7.6496
- MSE: 38,232.89
- RMSE: 195.53
- R-squared: 0.9993
- MAPE: 0.2607

A plot of Actual vs. Predicted Shares shows a strong alignment between the predicted and actual values, illustrating the model's accuracy.

#### Next Steps
1. **Hyperparameter Tuning**: Continue to refine models like XGBoost and SVM for better performance.
2. **Feature Engineering**: Explore additional features or transformations to improve model accuracy.
3. **Deployment**: Implement the RandomForest model in a production environment to predict shares in real-time.
4. **Further Analysis**: Investigate specific features' impact on share counts for deeper insights.
