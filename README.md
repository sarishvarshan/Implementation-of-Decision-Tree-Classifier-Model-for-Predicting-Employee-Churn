# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas module and import the required data set.
2. Find the null values and count them.
3. Count number of left values.
4. From sklearn import LabelEncoder to convert string values to numerical values.
5. From sklearn.model_selection import train_test_split.
6. Assign the train dataset and test dataset.
7. From sklearn.tree import DecisionTreeClassifier.
8. Use criteria as entropy.
9. From sklearn import metrics.
10. Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: sarish Varshan V
RegisterNumber:  212223230196
*/
```



## Output:
```
import pandas as pd
data=pd.read_csv("C:/Users/giri9/Downloads/Employee (1).csv")
data.head()
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/279081a5-d874-466e-8460-ff9d3cd5d7b1)
```
data.info()
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/64601e0d-d874-401b-b932-fbc8bac843a0)
```
data.isnull().sum()
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/d8f578e5-525b-4fe2-9151-71390ebec05c)
```
data['left'].value_counts()
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/f4f3a9bc-8b6e-4d64-bb17-02b75c695fd0)
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data.head()
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/7aa82992-ebc4-4183-a09a-2222f16f6791)
```
x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/7a7f9309-b27f-4e97-aef3-c4938f0eeea2)
```
y=data['left']
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_predict)
accuracy
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/a05a2a22-0f5e-4409-90cb-6fa03c576d46)
```
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/152167665/3ad741cc-768c-42f9-abe9-d5cfeea28eb1)






## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
