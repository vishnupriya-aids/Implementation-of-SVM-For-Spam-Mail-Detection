# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the spam mail dataset and preprocess the data.
 
2.Convert the email text into numerical features using TF-IDF.

3.Train the Support Vector Machine (SVM) classifier.

4.Test the model and evaluate it using accuracy and confusion matrix.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Vishnupriya.E
RegisterNumber:25010444
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import SVC
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
data = pd.read_csv("C:/Users/Admin/Downloads/spam.csv")
data = data[['v1', 'v2']]
data.columns = ['label', 'message']
data['label'] = data['label'].map({'ham': 0, 'spam': 1})
X = data['message']
y = data['label']
vectorizer = TfidfVectorizer(stop_words='english')
X = vectorizer.fit_transform(X)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
model = SVC(kernel='linear')
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n")
print(classification_report(y_test, y_pred))
cm = confusion_matrix(y_test, y_pred)
print("\nConfusion Matrix:\n")
print(cm) 
*/
```

## Output:
<img width="601" height="396" alt="WhatsApp Image 2026-05-24 at 8 05 00 PM" src="https://github.com/user-attachments/assets/db4f5acd-a25e-4e27-b1cd-cc61dc2caea2" />



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
