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
```
import numpy as np
import matplotlib.pyplot as plt
# Independent variable (X)
X = np.array([0,1, 2, 3, 4, 5,6,7,8,9])

# Dependent variable (Y)
Y = np.array([1,3, 2, 5, 7, 8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
x_mean = np.mean(X)
y_mean = np.mean(Y)

```

```
numerator = 0
denominator = 0

for i in range(len(X)):
    numerator += (X[i] - x_mean) * (Y[i] - y_mean)
    denominator += (X[i] - x_mean) ** 2

m = numerator / denominator
c = y_mean - m * x_mean

print("Slope (m):", m)
print("Intercept (c):", c)
```

```
Y_pred = m * X + c

plt.scatter(X, Y, color='blue', label='Actual Data')
plt.plot(X, Y_pred, color='red', label='Regression Line')
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.show()
```
## Output

<img width="865" height="659" alt="image" src="https://github.com/user-attachments/assets/8d59ccc6-79c9-4524-b504-037e3fad9dcb" />
<br>
<img width="798" height="428" alt="image" src="https://github.com/user-attachments/assets/2b55fffd-57c1-44c6-8946-eb32563803c5" />
<br>
<img width="965" height="694" alt="image" src="https://github.com/user-attachments/assets/479564d6-4afd-4a8a-a6d5-62de2785463b" />
<br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
