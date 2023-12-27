# Python-Online-Course-Prediction
This project report presents the analysis and linear regression modeling and prediction of an online course dataset. The dataset contains information about online courses, including their names, categories, instructor ratings, reviews, student enrollment, and other relevant attributes. The objective of this project is to develop regression models to predict the average rating of online courses based on their features. <br><br>
## Feature observation and hypothesis 

Feature Observations:
•	cbrt_Enrollment: This feature represents the highest correlation between cbrt_NumberRatings with 0.907349
•	cbrt_Review: This feature represents second highest correlation between cbrt_NumberRatings with 0.530124
•	cbrt_Student: This feature represents third highest correlation between cbrt_NumberRatings with 0.479917
<br><br><br>
![image](https://github.com/fdurmaz1/SQL_Company_project/assets/133916817/71305d69-f296-428f-b089-4d234499a1f9)

## Linear Regression with Lasso Report 

For the linear regression model with Lasso, we utilized the Lasso algorithm and performed feature selection based on different alpha values. We tested multiple alpha values (0.001, 0.01, 0.1, 1.0, and 10.0) and evaluated the performance of each model using R^2 (coefficient of determination) and RMSE (root mean squared error) metrics.
<br><br>
![image](https://github.com/fdurmaz1/SQL_Company_project/assets/133916817/d8975598-8e30-4f02-bc97-168d7c39fcaa)
<br><br>

The best performing model was obtained with an alpha value of 0.001, which yielded an R^2 of 0.900722  and an RMSE of 1.754775. The features used in this model were the same as the ones selected in the correlation-based feature selection. Moreover I find out this asso model will be the best for this dataset to predict NumberRatings. 
<br><br>
![image](https://github.com/fdurmaz1/SQL_Company_project/assets/133916817/16ab115c-2976-4464-80f8-2eae08c03c9c)
## Analysis 

To be analyze the findings and discuss why a specific linear model or feature selection method performed better than the others.
Based on the provided summary DataFrame, it sshows that the Lasso linear model with an alpha value of 0.001 performed the best, achieving a R2 score of 0.900722 and a lowest RMSE value of 1.754775. This indicates that the Lasso model was able to capture the underlying forrecast in the data effectively and make accurate predictions.<br>
Regarding the feature selection methods, all three methods (Correlation selection, Variance Threshold selection, SelectKBest selection) without feature transformation achieved the almost same R2 and RMSE values.
On the other hand, the feature transformation technique using the Log1p transformation has resulted in slightly lower R2 and higher RMSE values compared to the models without transformation. This shows that log1p transformation might not be good to use for this dataset.
To conclude , the best linear model overall is the Lasso model with an alpha value of 0.001. It performed better than other models in terms of accuracy and error metrics. The Lasso model stands out because it can select important features and leading to improved performance. The Lasso model's ability to select relevant features and control overfitting contributed to its superior performance in this case.
