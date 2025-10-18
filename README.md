# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```py
import numpy as np

# Input data
X = np.array(list(map(int,input().split())))
y = np.array(list(map(int,input().split())))

# Step 1: Calculate means
mean_x = np.mean(X)
mean_y = np.mean(y)

# Step 2: Calculate slope (m) and intercept (b)
m = np.sum((X - mean_x) * (y - mean_y)) / np.sum((X - mean_x)**2)
b = mean_y - m * mean_x

# Step 3: Predict values
y_pred = m * X + b

# Step 4: Print results
print(f"{m:.2f} {b:.2f}")
for i in y_pred:print(f"{i:.2f}",end=" ")
```
## Output
<img width="1285" height="351" alt="image" src="https://github.com/user-attachments/assets/50b38878-bdc5-43cf-ace7-2d948bfe43d6" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
