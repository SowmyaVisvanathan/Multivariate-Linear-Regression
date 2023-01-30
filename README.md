# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas as pd

### Step2
Import linear_model from sklearn

### Step3
Make a list of the independent values and call this variable X.Put the dependent values in a variable called y.

### Step4
From the sklearn module we will use the LinearRegression() method to create a linear regression object.

### Step5
Now we have a regression object that are ready to predict CO2 values based on a car's weight and volume:


## Program:
```
import pandas as pd
from sklearn import linear_model
df=pd.read_csv("car.csv") 
x=df[[ 'Weight', 'Volume']]
y=df['C02']

regr=linear_model. LinearRegression() 
regr.fit(x,y)

print("Coefficient:",regr.coef_) 
print("Intercept: ",regr.intercept_) 
predictedC02=regr.predict([[3300,1300]]) 
print("Predicted CO@ for the corresponding weight and volume", predictedC02)


```
## Output:
![output](/out.png)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.