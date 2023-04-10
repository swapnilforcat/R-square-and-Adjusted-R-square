# R-square-and-Adjusted-R-square
Understanding r-square and adjusted r-square and how they help in feature selection. Using Diabetes dataset from sklearn.


**1. R2** is a statistical measure that indicates how well a regression model fits the data. It is calculated as the proportion of the variance in the dependent variable that is explained by the independent variables in the model. The formula for calculating R2 is:

R2 = 1 - (SSres / SStot)

where:

SSres (sum of squares of residuals) represents the variation in the dependent variable that is not explained by the independent variables. It is calculated by summing the squared differences between the predicted values and the actual values of the dependent variable.
SStot (total sum of squares) represents the total variation in the dependent variable. It is calculated by summing the squared differences between the actual values of the dependent variable and the mean of the dependent variable.
R2 is then calculated by subtracting the ratio of SSres and SStot from 1. R2 ranges from 0 to 1, where a value of 1 indicates that the regression model perfectly fits the data, and a value of 0 indicates that the regression model does not fit the data at all.

In summary, R2 is calculated as the proportion of the variance in the dependent variable that is explained by the independent variables in the regression model.

**2. Adjusted R2** is a modified version of R2 that adjusts for the number of predictors or independent variables used in the regression model. The formula for adjusted R2 is:

Adjusted R2 = 1 - [(1-R2)*(n-1)/(n-k-1)]

where:

R2 is the unadjusted R2 value.
n is the sample size.
k is the number of independent variables or predictors in the model.
Adjusted R2 penalizes the inclusion of unnecessary variables in the model by adjusting the R2 score downward, relative to the number of variables used. The adjustment factor in the formula is based on the degrees of freedom, which is the number of observations minus the number of parameters estimated in the model. The adjustment factor is larger when the number of variables in the model increases, which reduces the value of adjusted R2.

In summary, adjusted R2 is calculated using a formula that adjusts the R2 value based on the number of predictors or independent variables used in the regression model. The adjustment factor in the formula penalizes the inclusion of unnecessary variables in the model, resulting in a more accurate measure of the model's fit to the data.


**R2 and adjusted R2** are both measures of how well a model fits a set of data. However, there is an important difference between the two that relates to the number of variables or predictors in the model.

R2 is a measure of the proportion of variation in the dependent variable (the variable being predicted) that is explained by the independent variables (the variables used to make the prediction). It ranges from 0 to 1, where 1 represents a perfect fit. However, R2 can be misleading when the model includes more variables. As the number of variables in the model increases, R2 increases, regardless of whether the added variables improve the model's accuracy. This is because R2 always increases when more variables are added, even if the added variables have little or no predictive power.

Adjusted R2, on the other hand, is a modified version of R2 that adjusts for the number of variables in the model. It takes into account the fact that adding more variables to the model will always increase R2, even if the added variables are not useful for prediction. Adjusted R2 penalizes the inclusion of unnecessary variables in the model by adjusting the R2 score downward, relative to the number of variables used. This means that the adjusted R2 score will be lower than the R2 score when there are many variables in the model, and higher when there are fewer variables in the model.

In summary, the main difference between R2 and adjusted R2 is that R2 gives a measure of how well the model fits the data, while adjusted R2 provides a more accurate measure of the model's fit, by taking into account the number of variables used in the model.
