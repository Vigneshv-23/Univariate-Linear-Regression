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
![WhatsApp Image 2023-12-24 at 15 47 59_2ffba023](https://github.com/Vigneshv-23/Univariate-Linear-Regression/assets/110780412/47d7e64e-e7a7-413e-a026-f484e2a08aee)

4.	Compute the y -intercept of the line by using the formula:
![WhatsApp Image 2023-12-24 at 15 48 20_33d3bab2](https://github.com/Vigneshv-23/Univariate-Linear-Regression/assets/110780412/3aa63e04-967d-447f-b2a2-eea0df14e2b8)

5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np
import matplotlib.pyplot as plt
x=np.array([1,8,6,5,4,15,20,56,47,29])
y=np.array([47,9,25,36,12,78,69,71,23,56])
plt.scatter(x,y)
plt.show()
xmean=np.mean(x)
ymean=np.mean(y)
num=0
den=0
for i in range(len(x)):
 num+=(x[i]-xmean)*(y[i]-ymean)
 den+=(x[i]-xmean)**2
m=num/den
b=ymean-m*xmean
print(m,b)
ypred=m*x+b
print(ypred)
plt.scatter(x,y,color='blue')
plt.plot(x,ypred,color='black')
plt.show()
```
## Output
![image](https://github.com/Vigneshv-23/Univariate-Linear-Regression/assets/110780412/1c0c417d-b061-40ce-b924-8f3210c9c79b)
![image](https://github.com/Vigneshv-23/Univariate-Linear-Regression/assets/110780412/391f933c-1781-4ca2-ab21-5f4232747090)



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
