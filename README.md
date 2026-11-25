# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries(numpy,pandas,scikit-learn).
<br>

### Step2
Load the dataset and separate the independent variables(X) and dependent variable(y).
<br>

### Step3
Split the data into training and testing sets.
<br>

### Step4
Create a LinearRegession model and train it using the training data.
<br>

### Step5
Predict the output for the test data and display the coefficients,intercept and R**2 score.
<br>

## Program:
```
 #Dataset Setup - Run this cell before starting the experiment

#Developed by:Mariya Asna k
#Register no:26018761
import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

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
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e0a77ea3-64b1-48ee-89b8-d26ae7f70c15" />


### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
