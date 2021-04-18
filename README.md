# Predicting-heart-disease
# Link to my presentation: https://www.youtube.com/watch?v=X8atLJJH9F8&feature=youtu.be
## Problem statement
World Health Organization has estimated 12 million deaths occur worldwide, every year due to Heart diseases. Half the deaths in the United States and other developed countries are due to cardio vascular diseases. The early prognosis of cardiovascular diseases can aid in making decisions on lifestyle changes in high risk patients and in turn reduce the complications. This research intends to pinpoint the most relevant/risk factors of heart disease as well as predict the overall risk using logistic regression. Using logistic regression I will be able to determine whether a person run the risk of having a heart disease. The classification goal is to predict whether the patient has 10years risk of future coronary heart disease.
## Motivation
WHO estimated that more than 12million people die from heart diseases each year. 12million is a very large number and there's a need to reduce this number to the minimum. Developing a classification model is essential such that one will be able to determine who runs a risk of a heart disease to take preventive measures. 
## Business goal
I am required to use logistic regression to predict whether a patient has 10years risk of future coronary heart disease or not. I will make use of binary logistic regression in which target variable has only two possible outcomes such as heart disease or no heart disease. Hospitals and Doctors may use this model to predict which patient is at risk and preventive measures to be taken
## Data Source
The dataset is publically available on the Kaggle website, and it is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has 10-year risk of future coronary heart disease (CHD).
## Model: Logistic Regression
Classification techniques are an essential part of machine learning and data mining applications. Approximately 70% of problems in Data Science are classification problems. There are lots of classification problems that are available, but the logistics regression is common and is a useful regression method for solving the binary classification problem

## Looking at the first five rows of my clean data framinhgahm.head()

![Capturefr](https://user-images.githubusercontent.com/63025220/95895835-4c66fb80-0d59-11eb-829b-d89ef838cba9.PNG)

## Data visualization
This involves undrestanding my dataset by placing it in a visual context so that patterns, trends and  correlations that might not otherwise be detected can be exposed

### Pair plot
Its build on histogram and scatter plot
![cap1](https://user-images.githubusercontent.com/63025220/95897584-c9937000-0d5b-11eb-996b-e62304d84962.PNG)
![Capture2](https://user-images.githubusercontent.com/63025220/95897639-ddd76d00-0d5b-11eb-9b49-7326da3cb93a.PNG)

### Finding correlation

![4](https://user-images.githubusercontent.com/63025220/95898329-dfedfb80-0d5c-11eb-8e3a-185e13bc874e.PNG)
  ![Capture5](https://user-images.githubusercontent.com/63025220/95898368-ef6d4480-0d5c-11eb-9742-00ae5996cc92.PNG)

## Logistic Regression
Logistic Regression is one of the most simple and commonly used Machine Learning algorithms for two-class classification.
Before applying this model on my data , I will have to split my data into training and test data

### Data splitting to training and testing model
sklearn.model_selection is the library use to split our data into training and testing dataset.

### 80% will be traing data and 20% testing data

## Model Development and Prediction
First, import the Logistic Regression module and create a Logistic Regression classifier object using LogisticRegression() function.

Then, fit your model on the train set using fit() and perform prediction on the test set using predict().

from sklearn.linear_model import LogisticRegression

logreg = LogisticRegression()

logreg.fit(X_train,y_train)

y_pred=logreg.predict(X_test)

## Model Evaluation using Confusion Matrix
A confusion matrix is a table that is used to evaluate the performance of a classification model

from sklearn import metrics

cnf_matrix = metrics.confusion_matrix(y_test, y_pred)

cnf_matrix

![Capture6](https://user-images.githubusercontent.com/63025220/95900242-9a7efd80-0d5f-11eb-92d6-7d5f5c0617df.PNG)

The dimension of this matrix is 2*2 because this model is binary classification.

## Visualizing Confusion Matrix using Heatmap

Let's visualize the results of the model in the form of a confusion matrix using matplotlib and seaborn.

![Capture7](https://user-images.githubusercontent.com/63025220/95901001-afa85c00-0d60-11eb-8181-c3e69365270d.PNG)

print("Accuracy:",metrics.accuracy_score(y_test, y_pred))

print("Precision:",metrics.precision_score(y_test, y_pred))


![Capture8](https://user-images.githubusercontent.com/63025220/95901217-00b85000-0d61-11eb-8f51-9897fa54ca83.PNG)

## My accuracy is 86%, considered as good accuracy.

## ROC Curve
Receiver Operating Characteristic(ROC) curve is a plot of the true positive rate against the false positive rate

![Capture9](https://user-images.githubusercontent.com/63025220/95901724-c1d6ca00-0d61-11eb-8bc1-0d181d693715.PNG)

AUC score for the case is 0.72. AUC score 1 represents perfect classifier, and 0.5 represents a worthless classifier.

## Limitation

It is vulnerable to overfitting

## Later work
I will be working with a dataset that requires me to use multinomial logistic regression in which the target variable has three or more nominal categories such as predicting the type of Wine.
## Conclusion
Model has adequately addressed the problem statement.It has also helped usunderstand how logistic regtression can be used to predict heart diseases

