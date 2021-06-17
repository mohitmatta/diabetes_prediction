# Diabetes Prediction

## _Predicting Diabetes - Evaluating biophysical Factors._

<a href="https://www.linkedin.com/in/mohit-matta-61b65b18"> Author: Mohit Matta </a>

<a href="https://mohitmatta.github.io/">Click here to go back to Portfolio Website </a>

![A remote image](https://mohitmatta.github.io/assets/img/work-analytics.jpg)

Abstract: 

Diabetes, often described as a “Disease of Civilization”, is a major public health problem that is approaching epidemic proportions globally. Undiagnosed diabetes can be predisposing factor to a fatal cardiac stroke. Its exponentially increasing cases has become a matter of concern world wide. Usually onset of type 2 diabetes happens in middle age and sometimes in old age. But nowadays incidences of this disease are reported in children as well. Risk factors leading to diabetes range from genetic susceptibility and body weight to food habits and lifestyle. Adult with diabetes have a two-to-three fold increased risk of heart attacks, neuropathy, foot ulcers, limb amputation and kidney failure. Early diagnosis is crucial and can be accomplished through relatively inexpensive testing of blood sugar. Diabetes can be controlled by promoting healthy diet and regular exercise, thereby reducing the growing global problem of overweight people and obesity.
Classification is one of the most important decision making techniques in many real world problem. In this work, the main objective is to classify the data as diabetic or non-diabetic and improve the classification accuracy. The main objective of our model is to achieve high accuracy.Classification accuracy can be increased if we use much of the data set for training and few data sets for testing.The aim of this project is to develop a system which can predict the diabetic risk level of a patient with a higher accuracy.

### Project Specific Questions
- What are the physical factors that are highly correlated?
- What are the physical factor directly leading to diabetes?
- Is diabetes gender neutral?
- Does agegroup play a role in diabetes?
- Do women with 2 pregnancies or more have a higher chance of diabetes than women with one or no pregnancy?
- what is the optimum value of k for kNN model that gives highest accuracy?
- Can Diabetes be predicted in an early stage using above analysis?
	

### Methods used in my project


1) Obtain the dataset
2) Clean our dataset
3) Explore/Visualize dataset to allow to find patterns and trends 
4) Model the data for predictive power
a) Apply Linear Regression model on dataset
b) Apply K-Nearest model on dataset
c) Apply decision tree algorithm on dataset
6) Interpret the data


### Project Dataset:

The dataset contains 9 columns and 2000 observations.The format is csv.Below are the column names and their description:

## Included Project Variables / Factors 

| Feature / Factors | Definition | 
| --------- | --------- | 
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration over 2 hours in an oral glucose tolerance test |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skin fold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index (weight in kg/(height in m)2) |
| DiabetesPedigreeFunction | Diabetes pedigree function (a function which scores likelihood of diabetes based on family history)|
| Age | Age (years) |
| Outcome | Class variable (0 if non-diabetic, 1 if diabetic) |



## R Libraries Used in this project


Package               Version
--------------------- ---------
- readr                 1.4.0
- dplyr                 1.0.6
- corrplot              0.88
- class                 7.3-19
- reprex                2.0.0
- ggplot2               3.3.3
- ggvis                 0.4.7
- MASS                  7.3-54
- magrittr              2.0.1
- caret                 6.0-88
- rpart                 4.1-15


## Repo Folder Structure

└───Datasets

└───Scripts

└───Results

## R Markdown Files 

| File Name  | Description |
| ------ | ------ |
| DIABETES_PREDICTION.Rmd | R Markdown file for extraction, EDA, Model |


## Datasets
| File  | Description |
| ------ | ------ |
| diabetes-2.csv | National Institute of Diabetes and Digestive and Kidney Diseases - https://www.kaggle.com/uciml/pima-indians-diabetes-database#diabetes.csv| 

## Results


The chi square test displayed the following statistics and proves that top three most relevant features are “Glucose”, “BMI” and “Number of times pregnant” because of the low p-values.“Insulin” and “Age” appear not statistically significant.From the table of deviance, we can see that adding insulin and age have little effect on the residual deviance.

![A remote image](https://github.com/mohitmatta/diabetes_prediction/blob/d07509838d7b9753f503eabe72090956edfa555b/Results/relevant_factors.png)


### Prediction
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/PredictionValuesExample.png?raw=true)
After feeding in the values for latitude, longitude and amenity information, my prediction code imputes the rest of the distance variables and makes pricing prediction.
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/PredictionValuesExampleResults.png?raw=true)
However, since my Renthop apartment inventory data is from 2017, my predicted prices are what can be expected from 4 years ago. Given that the rental market usually raises apartment prices by $90-$150 each year, I believe my prediction power is working correctly. The current rental price for the apartment in my example is 3482. Which is a difference of $530. Thus, supporting an increase of $132 in lease rents.

### Accuracy and MAE
![A remote image](https://github.com/adanque/RentalPricePrediction/blob/main/results/Accuracy_MAE_Results.png?raw=true)
Model Accuracy and MAE results are looking pretty interesting!
To measure the accuracy and loss of my model, I am using a set of my predicted values minus the actual target values between my train and test data. Then taking the mean of the absolute value of each in the set of values to divide this number by my target test values and then multiply by 100 to generate a mean absolute percentage error.  I then subtract 100 minus the mean absolute percentage error to produce accuracy metrics.


## References: 


1) https://www.academia.edu/36963831/Diabetes_Prediction_Using_Machine_Learning_Techniques 
2) https://www.frontiersin.org/articles/10.3389/fgene.2018.00515/full
3) https://www.kaggle.com/paultimothymooney/predict-diabetes-with-r-starter-kernel/data



:bowtie:
