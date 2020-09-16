## Introduction

 

Disease of the heart is considered the highest reason of death worldwide. One of the most frequent ways it can cause death is for the heart disease to cause a heart failure event. During this project, I will try to use historical data to build a machine learning model to predict whether a patient to experience death by a heart failure based on medical checks data and lifestyle habits. This can allow doctors to intervene and apply necessary measures to change the outcome for that patient.

 

## Data

 

To build a machine learning model, I will use a dataset from the website kaggle.com. The url for the data is: https://www.kaggle.com/andrewmvd/heart-failure-clinical-data. The data contains the following columns:

 

 

|Column|Description|
|-|-|
|Age| A numerical value for the age of test subject|
|Anaemia| A boolean value for whether the test subject has anameia|
|Creatinine Phosphokinase| The content of an enzyme that can indicate heart muscle damage|
|Diabetes|A boolean value for whether the test subject has diabetes|
|Ejection Fraction|Fraction of blood ejected from the left ventricle of the heart with each pump. It can be used to indicate heart failure or the severity of it|
|High Blood Pressure|A boolean value for whether the test subject has high blood pressure|
|Platelets|Platelet concentration in the blood measured in quantity per cubic millimeter|
|Serum Creatinine|Numerical value of creatinine in the blood serum. Indicator of kidney function|
|Serum Sodium|Numerical value of sodium in blood serum. |
|Sex| A boolean value, 0 for women, and 1 for men|
|Smoking|A boolean value for whether the test subject smokes|
|Time|The number of days between administring the tests and the follow up appointment and the determination of whether the patient has died or not|
|Death Event|A boolean value of whether the test subject has died after the medical tests|

 

Next, I will start with exploring the data for correlation and feature selection.

 

## Methodology

 

### Preprocessing Data

- After checking for missing data, the data appears to have none.

- A check was performed on data types to check the validity. Data types are compatible with actual attributes. Boolean values are already converted into binary 0 or 1. This should make it easier for further analysis with machine learning algorithms.

- Normalization of numerical data to be between 0 and 1 was performed to help produce a more accurate model.

- Visualization of the data was performed to detect best correlated variables.

 

## Feature Selection

Since we are trying to predict the patient will experience a heart failure leading to death right after the test, we will have to eliminate time as a feature. The idea is to intervene right away if we think the patient has high likelihood of death.

Also from the plot that can be seen in the notebook, we conclude that both sex and diabetes, have very low correlation with death event, so we will be eliminating those two features.

 

## Predictive Modeling

Our prediction target here is death event. We want to predict whether based on test results and lifestyle habits of a patient, whether the patient faces death in the near future. The nature of this problem is a classification issue. In order to do the prediction, we will use Decision Tree Model algorithm after splitting the data into training: 80% and test: 20%.

 

 

## Results

The result of model evaluation gives us a score of 78% accuracy. While these results are not perfect, they are high enough scores and can mean saving a lot of lives.

 

## Discussion

I believe that the results of our modeling were sufficiently accurate to be implemented after medical check up to predict the need of patients for immediate intervention. I also believe that with more data and more features to be tested, we can refine this model to produce an even more accurate representation of patients' likelihood to die of heart failure following a medical check up.

 

## Conclusing

In this project, I have studied the relationship between results of various medical tests and lifestyle habits on the possibility of patients to suffer from a heart episode leading to death. I believe that the model I produced could contribute to saving the lives of countless people and can also be improved with more data to eliminates any potential inaccuracies.

 
