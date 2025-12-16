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
Program to QR decomposition using the Gram-Schmidt method
Devloped By  : PRahathieswaran S 
Reference No : 25013305 
```
```
import numpy as np
def QR_Decomposition(A):
    n,m=A.shape
    Q=np.empty((n,m))
    u=np.empty((n,m))
    R=np.zeros((n,m))
    u[:,0]=A[:,0]
    Q[:,0]=u[:,0]/np.linalg.norm(u[:,0])
    for i in range(1,n):
        u[:,i]=A[:,i]
        for j in range(n):
            u[:,i]-=(A[:,i]@Q[:,j])*Q[:,j]
        Q[:,i]=u[:,i]/np.linalg.norm(u[:,i])
    for i in range(n):
        for j in range(i,m):
            R[i,j]=A[:,j]@Q[:,i]
    print(f"The Q Matrix is\n {Q}")
    print(f"The R Matrix is\n {R}")
    
a = np.array(eval(input()))
QR_Decomposition(a)
```
## OutputX
</br>
</br>
</br>
</br>
<img width="566" height="740" alt="image" src="https://github.com/user-attachments/assets/3015543f-7fd7-45e3-aa25-d7d82589b583" />
<img width="869" height="340" alt="image" src="https://github.com/user-attachments/assets/3caf58af-6d51-4123-b8e0-75773d0feedb" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
