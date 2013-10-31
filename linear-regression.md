# Linear Regression

## Overview
Training Set
  * x^(i) := i-th input
  * y^(i) := i-th output

Hypothesis Function
  * h_\theta(x) = \theta_0 + \theta_1x

Cost Function
  * J(\theta_0, \theta_1) = (1/2m)\sum_{i=1}^m(h_\theta(x^(i)) - y^(i))^2

The goal is to minimize J(\theta_0, \theta_1). 

## Gradient Descent Minimization

```text
repeat until convergence {
 \theta_j := \theta_j - \alpha\frac{\deltaJ(\theta_0, \theta_1)}{\delta\theta_j}
 simultaenously updating all values of \theta_j (i.e. do not iterate model parameters sequentially)
}
```

for linear equations, this becomes:
```text
repeat until convergence {
 \theta_0 := \theta_0 - \alpha\frac{1}{m}\sum_{i=1}^{m}(h_\theta(x^{(i)}) - y^{(i)})
 \theta_1 := \theta_1 - \alpha\frac{1}{m}\sum_{i=1}^{m}(h_\theta(x^{(i)}) - y^{(i)})x^{(i)}
}
```

 * If \alpha is too low, descent is slow
 * If \alpha is too large, iteration will overshoot and may diverge
