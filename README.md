# Probability Density Function Learning Using Roll-Number-Based Non-Linear Transformation

## 📌 Overview
This project demonstrates how to learn a probability density function (PDF) from air quality data using a roll-number-parameterized non-linear transformation. The approach combines statistical modeling with controlled non-linearity.

## 📊 Dataset
- **Name:** India Air Quality Data  
- **Source:** https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data  
- **Feature Used:** NO₂  

## 🔁 Step 1: Non-Linear Transformation
Each NO₂ value (*x*) is transformed into a new variable (*z*) using:
Where:
- `a_r = 0.05 × (r mod 7)`
- `b_r = 0.3 × (r mod 5 + 1)`
- `r` is the university roll number

## 📐 Step 2: Probability Density Learning
The transformed variable (*z*) is modeled using a Gaussian-shaped PDF:
The parameters are estimated using Maximum Likelihood Estimation (MLE):

- **μ (Mean):** Mean of transformed values  
- **σ (Standard Deviation):** Standard deviation of transformed values  
- **λ =** `1 / (2σ²)`  
- **c =** `1 / √(2πσ²)`

## 📊 Results
The parameters **λ**, **μ**, and **c** are automatically computed from the transformed data.

## 📈 Visualization
A histogram of the transformed values (*z*) is plotted along with the learned PDF curve to validate the model fit.

## 🛠 Tools & Libraries
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Google Colab  

## 🚀 How to Run
1. Upload `data.csv` to Google Colab.  
2. Replace `YOUR_ROLL_NUMBER` in the notebook with your university roll number.  
3. Run all cells to generate the results and plots.
