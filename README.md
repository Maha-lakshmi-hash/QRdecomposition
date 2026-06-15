# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
import os 
os.environ["OPENBLAS_NUM_THREADS"]="1"

matrix = eval(input())

rows = len(matrix)
cols = len(matrix[0])

max_sum = 0

for j in range(cols):
    col_sum = 0
    for i in range(rows):
         col_sum += abs(matrix[i][j])
    
    if col_sum > max_sum:
        max_sum = col_sum
        
print(f"{max_sum:.2f}")

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np

matrix = eval(input())

A = np.array(matrix)

norm = np.linalg.norm(A, 2)

print(f"{norm:.2f}")

import os

os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np

matrix =  eval(input())

A = np.array(matrix)

norm = np.linalg.norm(A, np.inf)

print(f"{norm:.2f}")






```

## Output
```
<img width="1160" height="666" alt="image" src="https://github.com/user-attachments/assets/c8f5b8e1-a2a1-4d5f-a3c7-a9de406567b5" />




```

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
