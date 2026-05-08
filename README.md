<img width="602" height="808" alt="Screenshot 2026-05-08 144230" src="https://github.com/user-attachments/assets/c31453bb-7ce9-437e-9758-9e0c99e7d4eb" />
<img width="602" height="808" alt="Screenshot 2026-05-08 144230" src="https://github.com/user-attachments/assets/9042e89f-5b7d-4007-818c-ce49455d8224" />
# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
#Ex 08 - Implementation of Decision Tree Classifier Model for Predicting Emp
# Import libraries
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import confusion_matrix, accuracy_score, classificatio
from sklearn import tree
import matplotlib.pyplot as plt
# ------------------------------
# Step 1: Sample dataset
# ------------------------------
data = {
 'satisfaction_level': [0.38, 0.80, 0.11, 0.72, 0.37, 0.41, 0.10, 0.92],
 'last_evaluation': [0.53, 0.86, 0.88, 0.87, 0.52, 0.50, 0.77, 0.89],
 'number_project': [2, 5, 7, 5, 2, 2, 6, 5],
 'average_monthly_hours': [157, 262, 272, 223, 159, 153, 247, 224],
 'time_spend_company': [3, 6, 4, 5, 3, 3, 4, 5],
 'Work_accident': [0, 0, 0, 0, 0, 0, 0, 0],
 'promotion_last_5years': [0, 0, 0, 0, 0, 0, 0, 0],
 'Departments': ['sales','accounting','hr','technical','support','managem
 'salary': ['low','medium','medium','high','low','low','medium','high'],
 'left': [1, 1, 1, 1, 1, 0, 1, 0] # Target variable: 1=Churn, 0=Stayed
}
df = pd.DataFrame(data)
# ------------------------------
# Step 2: Encode categorical variables
# ------------------------------
df = pd.get_dummies(df, columns=['Departments','salary'], drop_first=True)
# ------------------------------
# Step 3: Split into features and target
# ------------------------------
X = df.drop('left', axis=1)
y = df['left']
# ------------------------------
# Step 4: Train-test split
# ------------------------------
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, r
# ------------------------------
# Step 5: Create Decision Tree Classifier
# ------------------------------
dt_model = DecisionTreeClassifier(criterion='entropy', max_depth=4, random_
dt_model.fit(X_train, y_train)
# ------------------------------
# Step 6: Make predictions
# ------------------------------
y_pred = dt_model.predict(X_test)
# ------------------------------
# Step 7: Evaluate the model
# ------------------------------
print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
print("\nAccuracy Score:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))
# ------------------------------
# Step 8: Visualize the decision tree
# ------------------------------
plt.figure(figsize=(20,10))
tree.plot_tree(dt_model, feature_names=X.columns, class_names=['Stayed','Ch
plt.show()
```

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: BRINDHA A R
RegisterNumber: 212225040050 


## Output:
![decision tree classifier model](sam.png)
<img width="602" height="808" alt="Screenshot 2026-05-08 144230" src="https://github.com/user-attachments/assets/fa4b4f2f-d458-45bb-a130-b774c9c18eb6" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
