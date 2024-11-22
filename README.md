# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages and print the present data.
2. Print the placement data and salary data.
3. Find the null and duplicate values.
4. Using logistic regression find the predicted values of accuracy , confusion matrices.
5. Display the results.
## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by:MADHAN C
RegisterNumber:24004329
import pandas as pd
data=pd.read_csv(r"C:\Users\admin\Desktop\Placement_Data.csv")
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull().sum()
data1.duplicated().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
x=data1.iloc[:,:-1]
x
y=data1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import confusion_matrix
confusion=confusion_matrix(y_test,y_pred)
confusion
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]]) 
*/
```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)
## HEAD
![Screenshot 2024-11-22 090954](https://github.com/user-attachments/assets/bb6bff3c-a99d-4d8d-a484-2c74b5e59d43)
## COPY
![Screenshot 2024-11-22 091113](https://github.com/user-attachments/assets/5a863227-ad99-431f-af88-1496a0e48e5e)
## FIT TRANSFORM
![Screenshot 2024-11-22 091235](https://github.com/user-attachments/assets/db816e03-b6c2-428e-8eaa-96769ab1a278)
## LOGISTIC REGRESSION
![Screenshot 2024-11-22 091411](https://github.com/user-attachments/assets/165cf504-de51-48ed-b3c6-ab02c6fbf760)
## ACCURACY SCORE
![Screenshot 2024-11-22 091449](https://github.com/user-attachments/assets/1649511b-b5fd-4250-b891-2deaa4cce070)
## CONFUSION MATRIX
![Screenshot 2024-11-22 091527](https://github.com/user-attachments/assets/c3d11d29-56f8-4e42-9d43-2ff3e454da04)
## CLASSIFICATION REPORT
![Screenshot 2024-11-22 091634](https://github.com/user-attachments/assets/b64f7359-f9b6-40f8-a80e-b594c48d5d7f)
## PREDICTION
![Screenshot 2024-11-22 091707](https://github.com/user-attachments/assets/9d65b8d7-11b9-4cf0-906b-429c7f249d6a)
## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
