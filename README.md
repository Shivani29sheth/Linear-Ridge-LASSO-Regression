# Linear-Ridge-LASSO-Regression

## Problem statement:

Implement Linear Regression, Ridge Regression, and LASSO algorithms on a small data set, e.g. the Boston Housing Dataset (https://scikit-learn.org/stable/modules/generated/sklearn.datasets. load_boston.html), and compare the performance of each algorithm.

## Solution

The learning objective for all the three models differ by the regularization of the L1 / L2 penalty parameters. For linear regression, the cost function is given by E(w) = w<sup>T</sup> X<sup>T</sup> Xw − 2w<sup>T</sup> X<sup>T</sup> y + y<sup>T</sup> y and the model weights are learned via the gradients computed by: (2X<sup>T</sup> X w − 2 X<sup>T</sup> y). For Ridge Regression, the cost function is given by E(w) = w<sup>T</sup> X<sup>T</sup> X w − 2 w<sup>T</sup> X<sup>T</sup> y + y<sup>T</sup> y + λ||w||<sup>2</sup> <sub>2</sub> and its gradients are computed by (2X<sup>T</sup> X w − 2 X<sup>T</sup> y + 2 λ w). For LASSO Regression, the cost functino is computed by E(w) = w<sup>T</sup> X<sup>T</sup> X w − 2 w<sup>T</sup> X<sup>T</sup> y + y<sup>T</sup> y + λ ||w||<sub>1</sub> and its gradients are computed by (2X<sup>T</sup> X w − 2 X<sup>T</sup> y + λ) if the weights are positive, (2X<sup>T</sup> X w − 2 X<sup>T</sup> y − λ) if the weights are negative, and between [−2X<sup>T</sup> y + λ, −2X <sup>T</sup> y − λ] if the weights are zero. As we see, the cost and gradients of all three models differ by their regularization methods which control the weight updation in each of the models.

### Linear Regression:

<img src="Regression_Results/Linear_loss.png" width="35%" height="35%">

<img src="Regression_Results/Linear_performance.png" width="35%" height="35%">

Mean Square Error: 21.0060543102941

<br>

### Ridge Regression:

<img src="Regression_Results/Ridge_loss.png" width="35%" height="35%">

<img src="Regression_Results/Ridge_performance.png" width="35%" height="35%">

Mean Square Error: 55.53465972319111

<br>

### LASSO:

<img src="Regression_Results/LASSO_loss.png" width="35%" height="35%">

<img src="Regression_Results/LASSO_performance.png" width="35%" height="35%">

Mean Square Error: 53.32452986795816
