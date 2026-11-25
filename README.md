# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required Pandas and Linear Regression libraries.

### Step2
Read the dataset using pd.read_csv().

### Step3
Select the independent variables (Weight, Volume) and dependent variable (CO2).

### Step4
Create and train the Linear Regression model using LinearRegression() and fit().

### Step5
Display the coefficients, intercept and predict the CO2 output for the given input values using predict().

## Program:
```
import pandas as pd
df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)


```
## Output:

<img width="1813" height="551" alt="Screenshot 2026-11-04 102541" src="https://github.com/user-attachments/assets/8dc7e8fe-86a6-4f2e-b68b-579df61852ed" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
