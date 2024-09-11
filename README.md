Diabetes Risk Factors Analysis

## Overview
This repository contains the code and analysis for identifying key risk factors contributing to diabetes using a dataset from the Behavioral Risk Factor Surveillance System (BRFSS) 2015 survey. The analysis focuses on understanding which health and lifestyle factors are most predictive of diabetes (or prediabetes) and aims to provide insights for early diagnosis and public health interventions.

## Objective
The objective of this project is to perform exploratory data analysis (EDA) and build predictive models to identify the most critical health indicators associated with diabetes. By understanding these factors, the analysis helps in developing strategies for diabetes prevention and management.

## Dataset
Given csv file contains data sampled from the Behavioral Risk Factor Surveillance System (BRFSS) data. BRFSS is a health-related telephone survey that is collected annually by the CDC. Each year, the survey collects responses from over 400,000 Americans on health-related risk behaviors, chronic health conditions, and the use of preventative services. It has been conducted every year since 1984. This original dataset for 2015 year contains responses from 441,455 individuals and has 330 features. The given sample data is a clean dataset of 70,692 survey responses. It has an equal 50-50 split of respondents with no diabetes and with either prediabetes or diabetes. The target variable Diabetes_binary has 2 classes. 0 is for no diabetes, and 1 is for prediabetes or diabetes. This dataset has 21 feature variables and is balanced.

### Variables

- `Diabetes_binary` - 0 is for no diabetes, and 1 is for prediabetes or diabetes
- `HighBP` - (Blood Pressure) 0 = no high BP 1 = high BP
- `HighChol` - 0 = no high cholesterol 1 = high cholesterol
- `CholCheck` - 0 = no cholesterol check in 5 years 1 = yes cholesterol check in 5 years
- `BMI` - Body Mass Index
- `Smoker` - Have you smoked at least 100 cigarettes in your entire life? [Note: 5 packs = 100 cigarettes] 0 = no 1 = yes
- `Stroke` - (Ever told) you had a stroke. 0 = no 1 = yes
- `HeartDiseaseorAttack` - coronary heart disease (CHD) or myocardial infarction (MI) 0 = no 1 = yes
- `PhysActivity` - physical activity in past 30 days - not including job; 0 = no 1 = yes
- `Fruits` - Consume Fruit 1 or more times per day 0 = no 1 = yes
- `Veggies` - Consume Vegetables 1 or more times per day 0 = no 1 = yes
- `HvyAlcoholConsump` - (adult men >=14 drinks per week and adult women>=7 drinks per week) 0 = no 1 = yes
- `AnyHealthCare` - Have any kind of health care coverage, including health insurance, prepaid plans such as HMO, etc. 0 = no 1 = yes
- `NoDocbcCost`- Was there a time in the past 12 months when you needed to see a doctor but could not because of cost? 0 = no 1 = yes
- `GenHlth` - Would you say that, in general, your health is on a scale of 1-5: 
1 = excellent 2 = very good 3 = good 4 = fair 5 = poor.
- `MentHlth` - days of poor mental health scale 1-30 days
- `PhysHlth` - physical illness or injury count of days in the past 30 days, on a scale of 1-30
- `DiffWalk` - Do you have serious difficulty walking or climbing stairs? 0 = no 1 = yes
- `Sex`- 0 = female 1 = male
- `Age` - Age in category (see mapping below) -
    *1 - (18 <= AGE <= 24)*
    *2 - (25 <= AGE <= 29)*
    *3 - (30 <= AGE <= 34)*
    *4 - (35 <= AGE <= 39)*
    *5 - (40 <= AGE <= 44)*
    *6 - (45 <= AGE <= 49)*
    *7 - (50 <= AGE <= 54)*
    *8 - (55 <= AGE <= 59)*
    *9 - (60 <= AGE <= 64)*
    *10 - (65 <= AGE <= 69)*
    *11 - (70 <= AGE <= 74)*
    *12 - (75 <= AGE <= 79)*
    *13 - (80 <= AGE <= 99)*
    *14 - Don’t know / Refused to answer / Missing*
    
- `Education` - Education category (see mapping below) -
*1, 2, 3 - Didn’t graduate high school
4 - Graduated high school
5 - Attended college or technical school
6 - Graduated college or technical school
9 - Don’t know / Refused to answer / Missing*
- `Income` - Income category (see mapping below) -
    
    1, 2 - income less than $15,000
    3, 4 - $15,000 <= income < $25,000
    5 - $25,000 <= income < $35,000
    6 - $35,000 to less than $50,000
    7, 8 - income >= $50,000
    9 - Don’t know / Not sure / Missing Respondents
    

[Link](https://docs.google.com/spreadsheets/d/1WHsNhdamxdBXMQG1MoZnJs3XNfwomBB-iirNkUv6gWA/edit?usp=sharing) to google spreadsheet ( download it as csv or copy to your drive)

Target Variable: Diabetes_binary (0 = no diabetes, 1 = prediabetes or diabetes)
Features: Health and lifestyle indicators including BMI, high blood pressure, cholesterol levels, physical activity, smoking status, etc.

Key Features in the Dataset
Health Conditions: High blood pressure, high cholesterol, stroke, heart disease
Lifestyle Factors: Physical activity, smoking, fruit/vegetable consumption, alcohol use
Socioeconomic Indicators: Income, education
General Health Measures: BMI, mental and physical health, general health status

## Project Structure
data/: Directory containing the dataset used in the analysis.
notebooks/: Jupyter notebooks containing the Python code for data analysis and modeling.
results/: Directory with output plots, correlation heatmaps, and model performance.
README.md: This file, describing the project and providing instructions.

## Analysis Workflow
1. Exploratory Data Analysis (EDA)
Analyzed the distribution of key health indicators between diabetic and non-diabetic individuals.
Plotted countplots and histograms for categorical and continuous variables.
Performed a correlation heatmap to understand relationships between variables.
2. Univariate Analysis of Key Features
Key features like BMI, high blood pressure, cholesterol, and physical activity were explored.
Visualized the relationship between diabetes and each health/lifestyle factor.
3. Correlation Heatmap
Generated a correlation heatmap to observe correlations between features and the target variable.
Identified BMI, General Health, and Physical Activity as significant predictors of diabetes.
4. Logistic Regression for Feature Importance
Built a logistic regression model to assess feature importance.
Found BMI, General Health, and High Blood Pressure to be the most significant predictors.
5. Decision Tree for Feature Importance
Used a decision tree classifier to further identify the most important features.
BMI and General Health emerged as the most crucial features for predicting diabetes.

## Key Insights

BMI: Strong correlation with diabetes. Obesity is a key risk factor.
Physical Activity: Lack of regular exercise is more common among diabetics.
Blood Pressure & Cholesterol: Individuals with high blood pressure and cholesterol are at higher risk.
Socioeconomic Factors: Lower income and education are linked to higher diabetes prevalence.

## Recommendations

Promote Healthy Lifestyles: Encourage regular physical activity and balanced diets to reduce diabetes risk.
Screening Programs: Routine monitoring of BMI, blood pressure, and cholesterol, especially in high-risk populations.
Targeted Public Health Efforts: Focus interventions on vulnerable groups with lower income and education.
