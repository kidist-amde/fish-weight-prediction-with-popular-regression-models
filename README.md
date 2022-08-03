# Fish-weight-prediction-with-popular-regression-models(scikit-learn-implmntation)


##  Linear regression modles
- Linear regression models are supervised machine learning algorithms which predicts target variable Y based on Independent variables X.

 $$Y = wx+ b$$

Where :-  
 -  w is intercept in the y-axis
 -  b is a slope
 - w and b are trainable parameters(also referred coefficients, weights). 
 The goal is to find w and b such that we minimize the cost function 
 
$${SS_(residuals)} = {\sum_{ i=1}^n}{({y_i-y'_i})^{2}}$$

- We update w and b using gradient descent algorithm until convergence.

$$ {w_n} = {w_c - lr * \\frac{\partial SS_(residuals)}{\partial w_c } }$$

Where
- ${w_c}$ is the current value of w
- ${w_n}$  is the new updated value of w

```diff
- Our problem is  MultipleLinear Regression. linear regression problem only has one independent variable
- impacting the slope of the relationship,but multiple regression incorporates multiple independent variables.
```
 $$Y = {w_1}{x_1}+{w_2}{x_2} + {w_3}{x_3}......{w_n}{x_n} + b$$

#### This proejct uses Fish market [kaggle dataset](https://www.kaggle.com/datasets/aungpyaeap/fish-market).

# EDA of the dataset 
## Pairwise relationships in a dataset
<img src="imgs/p.png">

## Visualize the outliers of the dataset
<img src =imgs/b.png>

## Distribution of the dataset after standardization and noise removal 
<img src =imgs/dist.png>

## Visualize relationships between variables of dataset
<img src =imgs/h.png>


# Results of the models 
   
    
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Linear_regression</th>
      <th>Decission_Tree</th>
      <th>Random_Forest</th>
      <th>XGboots_Regressor	</th>
      <th>LGBM_Regressor</th>
      <th>CatBoost_Regressor</th>
      <th>SGD_Regressor</th>
      <th>Kernel_Ridge</th>
      <th>Elastic_Net</th>
      <th>Bayesian_Ridge</th>
      <th>GradientBoosting_Regressor</th>
      <th>SVR</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>MSE</th>
      <td>0.08</td>
      <td>0.05</td>
      <td>0.02</td>
      <td>0.03</td>
      <td>0.03</td>
      <td>0.03</td>
      <td>0.10</td>
      <td>0.10</td>
      <td>0.52</td>
      <td>0.08</td>
      <td>0.03</td>
      <td>0.02</td>
    </tr>
       <tr>
      <th>MAE</th>
      <td>0.23</td>
      <td>0.16</td>
      <td>0.09</td>
      <td>0.13</td>
      <td>0.12</td>
      <td>0.10</td>
      <td>0.26</td>
      <td>0.26</td>
      <td>0.62</td>
      <td>0.23</td>
      <td>0.12</td>
      <td>0.09</td>
    </tr>
       <tr>
      <th>R_squred</th>
      <td>0.89</td>
      <td>0.94</td>
      <td>0.98</td>
      <td>0.96</td>
      <td>0.97</td>
      <td>0.97</td>
      <td>0.86</td>
      <td>0.86</td>
      <td>-3.87</td>
      <td>0.89</td>
      <td>0.97</td>
      <td>0.98</td>
    </tr>
  </tbody>
</table>
</div>



## A learning curve of a best model (LGBMRegressor)
<img src= imgs/lc.png>

##  Residual Plot
<img src= imgs/r.png>

## The best model actual value  vs prediction value plot 
<img src = imgs/win.png>

## Normal Q-Q plot of best model 
<img src = imgs/qq.png>

## Regplot of target vs prediction on validation data set
<img src = imgs/gg.png>

