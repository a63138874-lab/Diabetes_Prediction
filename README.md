Diabetes Prediction Project works in the following way:

1. Dataset Collection
You can use the diabetes dataset containing medical information of patients.
Example:
Pregnancies 	Glucose	    BMI	    Age   	Outcome
6	             148	     33.6	    50	      1
1      	       85	       26.6	    31	      0
Here:
Outcome = 1 → Diabetic
Outcome = 0 → Not Diabetic

2. Data Preprocessing
The data is divided into:

X = df.drop("Outcome", axis=1)
y = df["Outcome"]
X = Input features
y = Output (Diabetic or Not)

3. Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(...)
Typically:
80% data for training
20% data for testing
The model learns from training data and is evaluated on unseen test data.

4. Feature Scaling
scaler = StandardScaler()
Features have different ranges:
Age → 20–80
Glucose → 50–200
BMI → 15–50
Scaling brings them to a similar scale so the model learns more effectively.

5. Model Training
model = LogisticRegression()
model.fit(X_train, y_train)
The model studies patterns in historical patient records.
For example, it may learn that:
High glucose + high BMI + higher age → higher diabetes risk.
Normal glucose + healthy BMI → lower diabetes risk.

7. Prediction
Suppose a new patient has:
[6,148,72,35,0,33.6,0.627,50]
The model processes these values and predicts:
prediction = model.predict(input_data_scaled)

Output:
[1]
Meaning:
Diabetic
or
[0]
Meaning:
Not Diabetic

7. Accuracy Calculation
accuracy_score(y_test, y_pred)
This checks how many predictions were correct on the test data.
Example:
Accuracy = 78%
This means the model correctly predicted about 78 out of every 100 cases in the test set.

Complete Flow
Dataset
   ↓
Preprocessing
   ↓
Train-Test Split
   ↓
Feature Scaling
   ↓
Train Logistic Regression Model
   ↓
Save Model
   ↓
Enter New Patient Data
   ↓
Model Prediction
   ↓
Diabetic / Not Diabetic



# Diabetes Prediction Using Machine Learning

## Overview
This project predicts whether a person is diabetic using Machine Learning.

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset
Pima Indians Diabetes Dataset

## Machine Learning Model
Logistic Regression

## Results
Achieved approximately 78% accuracy.

## Features
- Data preprocessing
- Feature scaling
- Model training
- Prediction system

Author - Ashvini Dound

