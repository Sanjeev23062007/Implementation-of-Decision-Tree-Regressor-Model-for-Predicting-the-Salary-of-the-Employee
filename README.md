# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Collect and preprocess the data (load dataset, handle missing values, select features and target).

2. Split the data into training and testing sets.

3. Train the Decision Tree Regressor on the training data.

4. Make predictions on the test data.

5. Evaluate the model performance using metrics like MAE, MSE, and R² score.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sanjeev A
RegisterNumber: 212224230246
*/
```
```
import pandas as pd
from sklearn.tree import DecisionTreeRegressor
from sklearn import metrics
data=pd.read_csv("/content/drive/MyDrive/Salary.csv")
data.head()
```
```
data.info()
```
```
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
```
```
r2=metrics.r2_score(y_test,y_pred)
r2
```
```
dt.predict([[5,6]])
```
## Output:

![image](https://github.com/user-attachments/assets/b6eb06ed-4ba7-4f88-b66d-965e386c76e7)

![image](https://github.com/user-attachments/assets/9d9d0104-9a89-4777-bf09-9842056a749e)

![image](https://github.com/user-attachments/assets/1635a14e-8d7d-4589-96fa-5f2262900a1c)

![image](https://github.com/user-attachments/assets/534f5c7c-4bf4-4f46-a02e-ce22492e7b43)

![image](https://github.com/user-attachments/assets/2e46c9ca-e69d-48f4-bc81-c7b9333e3457)

![image](https://github.com/user-attachments/assets/fa8cf2e0-9710-4a3c-934d-af4ea4403882)

![image](https://github.com/user-attachments/assets/c0d33f02-dbb1-43b5-8a98-3aefab0b35b5)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
