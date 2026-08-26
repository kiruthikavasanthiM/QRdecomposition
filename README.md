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
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
slope = num/den
c= Ymean-slope*Xmean
print(slope,c)
Y_pred= slope*X + c
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="green")
plt.show()

```

## Output
```
<img width="837" height="616" alt="image" src="https://github.com/user-attachments/assets/d8a6e42c-ebb0-42c9-a8de-aa0c3e07acf6" />

```

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
