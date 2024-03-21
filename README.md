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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Hoshini S 
RegisterNumber:  2305003006
*/
```
`````python
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input("Enter array X ")))
y=np.array(eval(input("Enter array Y ")))

#Calculting mean of X and Y
x_mean=np.mean(x)
y_mean=np.mean(y)
num,denom=0,0

for i in range (len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
    
#Calculating Slope:    
m=num/denom
print("\nSlope: ",m)

#Calculating Intercept:
b=y_mean-(m*(x_mean))
print("Intercept: ",b)

#Line equation:
y_predict=m*x+b
print(y_predict)

#Plotting graph:
plt.scatter(x,y)
plt.plot(x,y_predict,color="green")
plt.show()

#Sample:
#X=[8,2,11,6,5,4,12,9,6,1]
#y=[3,10,3,6,8,12,1,4,9,14]

#Predict y if x=3
y_3=m*3+b
print("If x=3 then y=",y_3)



## Output:
![95a2c616-f621-4236-91af-d03b96edda4a](https://github.com/hoshini28/Find-the-best-fit-line-using-Least-Squares-Method/assets/155607150/db068317-b3db-43d3-9284-12a35b98ce55)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
