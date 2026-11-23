# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries such as NumPy, Matplotlib and Scikit-learn.
2.Get the number of hours studied (X) and marks scored (Y) as input data.
3.Split the data into training and testing sets and create a Linear Regression model.
4.Train the model, predict the marks and plot the regression line.

## Program:
```py
# Program to implement the Simple Linear Regression Model
# for predicting the marks scored.

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Input data
X = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]).reshape(-1, 1)
Y = np.array([10, 20, 30, 40, 50, 60, 70, 80, 90, 100])

# Create Linear Regression model
model = LinearRegression()

# Train the model
model.fit(X, Y)

# Predict marks
predicted_marks = model.predict([[7.5]])

print("Slope:", model.coef_[0])
print("Intercept:", model.intercept_)
print("Predicted Marks:", predicted_marks[0])

# Plot the data
plt.scatter(X, Y, color='blue', label='Actual Marks')

# Plot regression line
plt.plot(X, model.predict(X), color='red', label='Regression Line')

plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression")
plt.legend()
plt.grid()
plt.show()
```

## Output:
Slope: 10.0

Intercept: 0.0

Predicted Marks: 75.0

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
