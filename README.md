# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
### Step 1: Start the program.

### Step 2: Import the NumPy library.

### Step 3: Define the coefficient matrix A and constant matrix B.

### Step 4: Form the augmented matrix [A∣B].

### Step 5: Apply Gaussian Elimination method to convert the matrix into upper triangular form.

### Step 6: Use back substitution to find the values of unknown variables.

### Step 7: Display the solution matrix.

### Step 8: Stop the program.
## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Ritesh DP
RegisterNumber: 212225040339
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero defected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %.2f' %(i,x[i]),end=' ')
```

## Output:
<img width="1039" height="529" alt="image" src="https://github.com/user-attachments/assets/f64dde71-4ece-4fe1-b9aa-db271cfc3c24" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

