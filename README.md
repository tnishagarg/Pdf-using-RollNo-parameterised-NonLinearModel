# Probability Density Function Learning Using Roll-Number-Based Non-Linear Transformation

##  Overview
This project demonstrates how to learn a probability density function (PDF) from air quality data using a roll-number-parameterized non-linear transformation. The approach combines statistical modeling with controlled non-linearity.

##  Dataset
- **Name:** India Air Quality Data  
- **Source:** https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data  
- **Feature Used:** NO2  

##  Step 1: Non-Linear Transformation
In this step, each value of the NO2 feature (denoted as *x*) is transformed into a new variable *z* using a roll-number-parameterized non-linear transformation function.

The transformation function is defined as:

T_r(x) = x + a_r*sin(b_r*x)

Thus, the transformed variable is given by:
z = T_r(x)
Where:
- `a_r = 0.05 × (rmod 7)`
- `b_r = 0.3 × (rmod 5 + 1)`
- `r` is the university roll number

##  Step 2: Probability Density Learning
The transformed variable (*z*) is modeled using a Gaussian-shaped PDF:
The parameters are estimated using Maximum Likelihood Estimation (MLE):

- **Mu (Mean):** Mean of transformed values  
- **Sigma (Standard Deviation):** Standard deviation of transformed values  
- **Lambda =** `1 / (2σ^2)`  
- **c =** `1 / sqrt(2πσ^2)`

##  Results
The learned parameters of the probability density function are shown below:

| Parameter | Value |
|---------|--------|
| Lambda | 0.0034046895152237 |
| Mu | 21.46564312301054 |
| c | 0.032920302733753855 |

