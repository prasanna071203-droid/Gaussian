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
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: PRASANNA P
RegisterNumber: 212225230214
*/
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

n=int(input())
a=[[float(input()) for j in range(n+1)] for i in range(n)]

for i in range(n):
    for j in range(i+1,n):
        f=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]-=f*a[i][k]

x=[0]*n

for i in range(n-1,-1,-1):
    x[i]=(a[i][n]-sum(a[i][j]*x[j] for j in range(i+1,n)))/a[i][i]

for i in range(n):
    print(f"X{i} = {x[i]:.2f}",end=" ")
```

## Output:
<img width="1039" height="529" alt="image" src="https://github.com/user-attachments/assets/f64dde71-4ece-4fe1-b9aa-db271cfc3c24" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

