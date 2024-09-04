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


```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: viswanadham venkata sai sruthi
RegisterNumber: 212223100061
import numpy as np
import matplotlib.pyplot as plt

# Example data
x = np.array([8,2,11,6,5,4,12,9,6,1])
y = np.array([3,10,3,6,8,12,1,4,9,14])

# Calculate the coefficients of the best fit line
A = np.vstack([x, np.ones(len(x))]).T
m, c = np.linalg.lstsq(A, y, rcond=None)[0]

# Display the result
print(f"Best fit line: y = {m:.2f}x + {c:.2f}")

# Plotting
plt.scatter(x, y, color='blue', label='Data Points')
plt.plot(x, m*x + c, color='red', label='Best Fit Line')
plt.xlabel('x')
plt.ylabel('y')
plt.legend()
plt.show()

```

## Output:
![OUTPUT](<Screenshot 2024-09-04 211330.png>)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
