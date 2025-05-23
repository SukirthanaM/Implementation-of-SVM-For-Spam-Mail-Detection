# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import Required Libraries.
2.  Use chardet to detect the encoding of the file spam.csv.
3.  Load the CSV file using the encoding (in this case, 'windows-1252').
4. Display the first few rows and general information. 
5. Ensure the dataset does not contain null or missing values.
6. Feature (x) = text messages (column "v2").
7. Label (y) = spam/ham classification (column "v1").
8. Split the Data into Training and Testing Sets.
9. Use CountVectorizer to convert text data into numerical vectors.
10. Use Support Vector Classifier to train on the vectorized data.
11. Predict whether messages are spam or not.
12. Use accuracy score to evaluate the model performance.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Sukirthana.M
RegisterNumber:  212224220112

import chardet
file='spam.csv'
print("Name: Sukirthana.M\nReg.no: 212224220112")
with open(file,'rb')as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()

data.info()

data.isnull().sum()

x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
![image](https://github.com/user-attachments/assets/4f02fdf7-d4ab-454f-8587-b59c3773415b)
![image](https://github.com/user-attachments/assets/6b5e5847-6252-480c-a13d-6e4de41c1330)
![image](https://github.com/user-attachments/assets/5db41d3f-76e9-45c9-ab07-d76c5405173f)

![image](https://github.com/user-attachments/assets/cacb5e4c-32de-4078-92a9-3335482fb860)

![image](https://github.com/user-attachments/assets/7dd5894f-b005-431d-aa36-ed1104cd0716)

![image](https://github.com/user-attachments/assets/221dd448-abba-43c9-9e20-6eb6e7062ee4)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
