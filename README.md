# Probability Density Function Learning Using Roll-Number-Based Non-Linear Transformation

##  Overview
This project demonstrates how to learn a probability density function (PDF) from air quality data using a roll-number-parameterized non-linear transformation. The approach combines statistical modeling with controlled non-linearity.

##  Dataset
- **Name:** India Air Quality Data  
- **Source:** https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data  
- **Feature Used:** NO₂  

##  Step 1: Non-Linear Transformation
Each NO₂ value (*x*) is transformed into a new variable (*z*) using:
Where:
- `a_r = 0.05 × (r mod 7)`
- `b_r = 0.3 × (r mod 5 + 1)`
- `r` is the university roll number

##  Step 2: Probability Density Learning
The transformed variable (*z*) is modeled using a Gaussian-shaped PDF:
The parameters are estimated using Maximum Likelihood Estimation (MLE):

- **μ (Mean):** Mean of transformed values  
- **σ (Standard Deviation):** Standard deviation of transformed values  
- **λ =** `1 / (2σ²)`  
- **c =** `1 / √(2πσ²)`

##  Results
The learned parameters of the probability density function are shown below:

| Parameter | Value |
|---------|--------|
| Lambda (λ) | 0.0034046895152237 |
| Mu (μ) | 21.46564312301054 |
| c | 0.032920302733753855 |

