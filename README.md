# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
Step 1- Import numpy library using import statement.
Step 2- Import sys library
Step 3- Create a variable n to recieve to recieve dimention
of the matrix.
Step 4- using input n,create a zero matrix 'a' of x(n+1)
and a zero row matrix 'x' of n using np.zeros.
Step 5- Initiate 1st nested for loop to get values
from user and store it in the 'a' matrix using float(input).
Step 6- Initiate 2nd nested for loop to apply
 gaussian elimination.
Step 7- Initiate 3rd nested for loop to calculate the
solution of the 'a' matrix using back substitution.
Step 8- Display the solution for each variable upto
2 decimals using for loop and printO with '%" operator.
```
## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Supraja.B
RegisterNumber: 2305002026

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range(n):
    for j in range(i+1, n):
        ratio = a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
```

## Output:
![image](https://github.com/Supraja0510/Gaussian/assets/155217478/0146c748-65fe-4641-8f9c-65d4d0621111)
![image](https://github.com/Supraja0510/Gaussian/assets/155217478/c9ad2537-38fe-4ea6-9b56-d284796b46e4)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

