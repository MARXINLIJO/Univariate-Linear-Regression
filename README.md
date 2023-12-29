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
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: MARXIN LIJO M
#register number: 212223240085
'''
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Orange')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output

![292743635-d36f67b6-1369-499e-9c5b-5ad4cd78d64a](https://github.com/MARXINLIJO/Univariate-Linear-Regression/assets/145742540/2da96557-0312-4d60-b24e-443b94d111d7)

![292743662-be0d9e36-903f-40f7-a3b4-49adfe333b7e](https://github.com/MARXINLIJO/Univariate-Linear-Regression/assets/145742540/5ff1f088-df1b-4485-abbc-3341dd4bb60e)
</br>
![292743669-b7482037-a4e4-43a1-bb6c-1e0a8f82dd7e](https://github.com/MARXINLIJO/Univariate-Linear-Regression/assets/145742540/322c5974-7ff8-4612-81cf-4aa9ba0759c7)
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
