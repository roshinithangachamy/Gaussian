# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First import numpy as np and enter the value for n
2. Enter the values of array 
3. Use for loop and get the values of i and j
4. Then print("X%d = %0.2f" %(i,res[i]),end =" ") to get the output

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:T.Roshini 
RegisterNumber:23011660
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n): 
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end =" ")
        
```

## Output:
![output](./![Alt text](<Guassian Elimination.png>))


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

