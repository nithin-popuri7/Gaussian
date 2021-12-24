# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by:Popuri.Siva Naga Nithin 
RegisterNumber:21003942 
'''
import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
X = np.zeros((n))
# reading augmented matric coefficients
for i in range((n)):
    for j in range(n+1):
        a[i][j]=float(input())
#applying gauss elimination
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('divide by zero detected!')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio*a[i][k]
# back substitution
X[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i] = a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i]
# displaying solution
for i in range(n):
    print('X%d = %0.2f' %(i,X[i]),end=' ')

         
*/
```

## Output:
![github logo](gausion.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

