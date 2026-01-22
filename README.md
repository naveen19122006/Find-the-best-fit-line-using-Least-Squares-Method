# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```python
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Naveen Kumar E
RegisterNumber: 212224230181 
*/

import matplotlib.pyplot as plt

X = [1, 2, 3, 4, 5]
Y = [2, 4, 5, 4, 5]

n = len(X)

mean_x = sum(X) / n
mean_y = sum(Y) / n

num = 0
den = 0
for i in range(n):
    num += (X[i] - mean_x) * (Y[i] - mean_y)
    den += (X[i] - mean_x) ** 2

m = num / den
b = mean_y - m * mean_x

y_pred = [m * x + b for x in X]

print(f"y = {m:.2f}x + {b:.2f}")

plt.scatter(X, Y)
plt.plot(X, y_pred)
plt.show()
```

## Output:
<img width="676" height="441" alt="image" src="https://github.com/user-attachments/assets/720622df-1f68-4a0c-a768-0759f4888ce5" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
