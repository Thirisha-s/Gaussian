# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
Step 1:
Import the numpy module to use the built-in functions for calculation.

Step 2:
Import the sys module to use the built-in functions.

Step 3:
Get input from the user for number of rows and add it by 1 for number of columns.

Step 4:
Using np.zeros() set the matrix as null matrix.

Step 5:
Using nested for loop get input from the user for each element in the matrix.

Step 6:
Using nested for loop find the ratio and perform the elementary row operations and find the final matrix.

Step 7:
Use back substitution method to find the value of the variables and print it.

Step 8:
End the program. 

## Program:
```python
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: s.thirisha
RegisterNumber: 22001920

import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=arr[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-arr[i][j]*x[j]
    x[i]=x[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")       
```

## Output:
![Screenshot_20230121_201615](https://user-images.githubusercontent.com/120380280/213872106-e15891ce-9a70-415c-a460-7634e5b614c3.png)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

