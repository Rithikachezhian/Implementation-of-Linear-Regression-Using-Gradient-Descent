# Implementation-of-Linear-Regression-Using-Gradient-Descent

AIM:

To write a program to predict the profit of a city using the linear regression model with gradient descent.

Equipments Required:

Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
Algorithm:
Import the required library and read the dataframe.
Write a function compute Cost to generate the cost function.
Perform iterations of gradient steps with learning rate.
Plot the Cost function using Gradient Descent and generate the required graph.


Program:

import numpy as np
import matplotlib.pyplot as plt

x = np.array([1, 2, 3, 4, 5], dtype=float)
y = np.array([2, 4, 6, 8, 10], dtype=float)

m = 0
c = 0
learning_rate = 0.01
iterations = 1000
n = len(x)

for i in range(iterations):
    y_pred = m * x + c

    dm = (-2/n) * np.sum(x * (y - y_pred))
    dc = (-2/n) * np.sum(y - y_pred)

    m = m - learning_rate * dm
    c = c - learning_rate * dc

print("Slope:", m)
print("Intercept:", c)

y_pred = m * x + c

print("Predicted Values:", y_pred)

plt.scatter(x, y, label="Actual Values")
plt.plot(x, y_pred, color="red", label="Regression Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Simple Linear Regression Using Gradient Descent")
plt.legend()
plt.show()


Output:

<img width="736" height="580" alt="image" src="https://github.com/user-attachments/assets/1d55ad12-d125-40fd-b1ee-3274cda54f0c" />

Result:

Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
