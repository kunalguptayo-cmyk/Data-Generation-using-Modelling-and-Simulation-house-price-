# Data Generation using Modelling and Simulation for Machine Learning

## Problem Description
This project focuses on generating synthetic house price data using a
simulation-based modelling approach and evaluating multiple machine learning
models to identify the best-performing model. The objective is to demonstrate
how simulation-generated data can be used effectively for machine learning
model comparison when real-world data is unavailable.

---

## Simulation Tool Used
Monte Carlo Simulation implemented using NumPy.

---

## Parameters and Bounds

| Parameter | Lower Bound | Upper Bound |
|---------|-------------|-------------|
| Area (sq ft) | 500 | 3000 |
| Rooms | 1 | 6 |
| Location Factor | 0.8 | 1.3 |
| Age of House (years) | 0 | 30 |

---

## Data Generation Method
Random values for each parameter were generated within predefined bounds using
a Monte Carlo simulation approach. These parameters were passed into a
mathematical pricing model that simulates real-world house prices. Random noise
was added to the model to represent market uncertainty and variability.

The simulated house price was computed as a weighted combination of area,
number of rooms, location factor, house age, and noise.

---

## Machine Learning Models Used
The following machine learning models were trained and evaluated on the
simulated dataset:

- Linear Regression  
- Ridge Regression  
- Lasso Regression  
- Decision Tree Regressor  
- Random Forest Regressor  

---

## Evaluation Metrics
The models were evaluated using the following metrics:

- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)  
- R² Score  

Lower values of MAE and RMSE indicate better predictive performance, while
higher R² values indicate a better fit.

---

## Results

The performance comparison of different machine learning models is shown
below:

| Rank | Model | MAE | RMSE | R² Score |
|----|------|------|------|---------|
| 1 | **Lasso Regression** | 40810.61 | **50862.32** | 0.999503 |
| 2 | Linear Regression | 40810.84 | 50862.75 | 0.999503 |
| 3 | Ridge Regression | 41085.16 | 50918.26 | 0.999502 |
| 4 | Random Forest | 136147.34 | 171199.81 | 0.994365 |
| 5 | Decision Tree | 215280.11 | 281631.92 | 0.984751 |

A bar chart comparing RMSE values was also generated to visually illustrate
model performance differences.

---

## Conclusion
Based on the experimental results, **Lasso Regression** achieved the lowest
RMSE and MAE while maintaining an extremely high R² score. This indicates that
the simulated house price data follows a predominantly linear relationship
with the input parameters.

Although tree-based models such as Random Forest and Decision Tree are capable
of capturing non-linear patterns, they did not perform as well on this
synthetically generated dataset due to the underlying linear nature of the
simulation model.

Hence, **Lasso Regression** is identified as the best-performing model for
house price prediction using simulation-generated data.

---

## Tools & Technologies Used
- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn  

---

## Author
Kunal Gupta
