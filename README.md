# Employee Performance Analysis

![Screenshot 2023-10-22 193606](https://github.com/RahiniSathish/EmployeePerformanceAnalysis/assets/141403412/0455ff85-5e71-4cbe-bca6-94a744e0ed9b)


This repository contains a data science project focused on analyzing and improving employee performance at INX Future Inc, a leading data analytics and automation solutions provider. The project aims to provide actionable insights into employee performance and recommendations to enhance it while maintaining a positive work environment.

# Project Structure

Project Summary

# Requirement:  
Data from third-party sources.
# Analysis: 
Interpreting data and summary of various choices, from selecting machine learning algorithms to data processing techniques.
# Summary: 
Project summary with analysis and recommendations.

# Data:

external: Data from third-party sources.


processed: The final, canonical data sets for modeling.


raw: The original, immutable data dump.

# src:

Data Processing: Jupyter notebooks for data processing, data munging, and exploratory analysis.
data_processing.ipynb

data_exploratory_analysis.ipynb

models: Scripts to train machine learning models and make predictions.

train_model.ipynb

predict_model.ipynb

references: Data dictionaries, manuals, and explanatory materials.



# Visualization

Visualization: Generate visualizations using the visualize.ipynb script.


visualization: Scripts for creating exploratory and results visualizations.

visualize.ipynb


# Getting Started

Data: Obtain the project data from INX_Future_Inc_Employee_Performance_CDS_Project2_Data_V1.8.xls and place it in the appropriate data 
directories (external, processed, or raw) as needed.

Data Processing: Explore and process the data using the Jupyter notebooks provided in the src/Data Processing directory.


Model Training: Use the scripts in the src/models directory to train machine learning models based on the processed data.


Predictions: Run the predict_model.ipynb script to make predictions using the trained model.


Summary and Recommendations: Refer to the Project Summary/Summary section for a comprehensive project summary with analysis and recommendations.

# Contributing
We welcome contributions to this project. If you have suggestions or improvements to share, please submit a pull request.

# License
This project is licensed under the MIT License - see the LICENSE file for details.


# Acknowledgments

We thank INX Future Inc for providing the data and supporting this analysis.
The project structure was inspired by the best practices for organizing data science projects.

## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Documentation

[Documentation](https://linktodocumentation)


## Task

# The Goal and Insights of the project are as follows:


   A trained model which can predict the employee performance based on factors as inputs. This will be used to hire employees Recommendations to improve the employee performance based on insights from analysis The given Employee dataset consist of 1200 rows. The features present in the data are 28 columns. The shape of the dataset is 1200x28. The 28 features are classified into quantitative and qualitative where 19 features are quantitative (11 columns consists numeric data & 8 columns consists ordinal data) and 8 features are qualitative. EmpNumber consist alphanumerical data (distinct values) which doesn't play a role as a relevant feature for performance rating.

From Correlation we can get the important aspects of the data, Correlation between features and Performance Rating.Correlation is a statistical measure that expresses the extent to which two variables are linearly related.The analysis of the project has gone through the stage of Univariate,Bivariate & Multivariate analysis, correlation analysis and analysis by each department to satisfy the project goal.

The dataset consists of Categorical data and Numerical data. The Target variable consist of ordinal data, so this is a classification problem.The multiple machine learning model used in this project is Support vector classifier, Random forest classifier & Artifical neural network[Multilayer percepton]. from above all models Artifical neural network[Multilayer percepton] predicts higher accuracy 95.80%.

One of the important goal of this project is to find the important feature affecting the performance rating. The important features were predicted using the machine learning model feature importance technique. The main technique used in the preprocessing data using the Mannual & Frequency encoding method to convert the string - categorical data into numerical data, because, Most of machine learning methods are based on numerical methods where strings are not supportive. The overall project was performed and achieved the goals by using the machine learning model and visualization techniques.

# 1. Requirement
The data was given from the IABAC for this project where the collected source is IABAC™. The data is based on INX Future Inc, (referred as INX ). It is one of the leading data analytics and automation solutions provider with over 15 years of global business presence. INX is consistently rated as top 20 best employers past 5 years. The data is not from the real organization. The whole project was done in Jupiter notebook with python platform.

# 2. Analysis
Data were analyzed by describing the features present in the data. the features play the bigger part in the analysis. The features tell the relation between the dependent and independent variables. Pandas also help to describe the datasets answering following questions early in our project. The data present in the dataset are divided into numerical and categorical data.

Categorical Features EmpNumber Gender EducationBackground MaritalStatus EmpDepartment EmpJobRole BusinessTravelFrequency OverTime Attrition

Numerical Features Age DistanceFromHome EmpHourlyRate NumCompaniesWorked EmpLastSalaryHikePercent TotalWorkExperienceInYears TrainingTimesLastYear ExperienceYearsAtThisCompany ExperienceYearsInCurrentRole YearsSinceLastPromotion YearsWithCurrManager

Ordinal Features EmpEducationLevel EmpEnvironmentSatisfaction EmpJobInvolvement EmpJobLevel EmpJobSatisfaction EmpRelationshipSatisfaction EmpWorkLifeBalance PerformanceRating

# 3.Univariate, Bivariate & Multivariate Analysis
Library Used: Matplotlib & Seaborn
Plots Used: Histplot, Lineplot, CountPlot, Barplot
Tip: All Observation or insights written below the plots
Univariate Analysis: In univariate analysis we get the unique labels of categorical features, as well as get the range & density of numbers

Bivariate Analysis: In bivariate analysis we check the feature relationship with target veriable.

Multivariate Analysis: In multivariate Analysis check the relationship between two veriable with respect to the target veriable.

# CONCLUSION 
There are some features are positively correlated with performance rating( Target variable) 
# [Emp Environment Satisfaction,Emp Last Salary Hike Percent,Emp Work Life Balance]

# 4.Explotary Data Analysis
Basic Check & Statistical Measures* Their is no constant column is present in Numerical as well as categoriacl data.

# Distribution of Continuous Features:
In general, one of the first few steps in exploring the data would be to have a rough idea of how the features are distributed with one another. To do so, we shall invoke the familiar distplot function from the Seaborn plotting library. The distribution has been done by both numerical features. it will show the overall idea about the density and majority of data present in a different level.

The age distribution is starting from 18 to 60 where the most of the employees are laying between 30 to 40 age count Employees are worked in the multiple companies up to 8 companies where most of the employees worked up to 2 companies before getting to work here. The hourly rate range is 65 to 95 for majority employees work in this company. In General, Most of Employees work up to 5 years in this company. Most of the employees get 11% to 15% of salary hike in this company.


# 5.Data Pre-Processing
Check Missing Value: Their is no missing value in data

Categorical Data Conversion: Handel categorical data with the help of frequency and mannual encoding, because feature is contain lot's of labels

Mannual Encoding: Mannual encoding is a best techinque to handel categorical feature with the help of map function, map the labels based on frequency.

Frequency Encoding: Frequency encoding is an encoding technique to transform an original categorical variable to a numerical variable by considering the frequency distribution of the data getting value counts.

Outlier Handling Some features are contain outliers so we are impute this outlier with the help of IQR because in all features data is not normally distributed

Feature Transformation: In YearsSinceLastPromotion some skewed & kurtosis is present, so we are use Square Root Transformation techinque

Scaling The Data: scaling the data with the help of Standard scalar
Standard Scaling: Standardization is the process of scaling the feature, it assumes the feature follow normal distribution and scale the feature between mean and standard deviation, here mean is 0 and standard deviation is always 1.
# 6.Future Selection
Drop unique and constant feature: Dropping employee number because this is a constant column as well as drop Years Since Last Promotion because we create a new feaure using square root transformation

Checking Correlation: Checking correlation with the help of heat map, and get the their is no highly correlated feature is present.

Heatmap: A heatmap is a graphical representation of data that uses a system of color-coding to represent different values.

Check Duplicates: In this data Their is no dupicates is present.

# 7.Machine learning Model Creation & Evaluation
Define Dependant and Independant Features:

Balancing the data: The data is imbalance, so we need to balance the data with the help of SMOTE


# Algorithm:
# AIM:
Create a sweet spot model (Low bias, Low variance)
HERE WE WILL BE EXPERIMENTING WITH THREE ALGORITHM

# Random Forest

Random forest very well perform in training data with 100% accuracy but in testing 95.61% after doing hyperparameter tunning testing score is decreases.

# 8.Saving Model
Save model with the helpof pickle file

Tools and Library Used:
Tools:
Jupyter

Library Used:
Pandas Numpy Matplotlib Seaborn pylab Scipy Sklearn Pickle

# Task

# Goal 1: Department Wise Performances
PLOT USED
CountPlot: countplot is used to Show the counts of observations in each categorical bin using bars. Sales: The Performace rating level 3 is more in the sales department. The male performance rating the little bit higher compared to female.
Human Resources: The majority of the employees lying under the level 3 performance . The older people are performing low in this department. The female employees in HR department doing really well in their performance.

Development: The maximum number of employees are level 3 performers. Employees of all age are performing at the level of 3 only. The gender-based performance is nearly same for both.

Data Science: The highest average of level 3 performance is in data science department. Data science is the only department where less number of level 2 performers. The overall performance is higher compared to all departments. Male employees are doing good in this department.

Research & Development: The age factor is not deviating from the level of performance here where different employees with different age are there in every level of performance. The R&D has the good female employees in their performance.

Finance: The finance department performance is exponentially decreasing when age increases. The male employees are doing good. The experience factor is inversely relating to the performance level.

# Goal 2: Top 3 Important Factors effecting employee performance
The top three important features affecting the performance rating are ordered with their importance level as follows,

Employment Environment Satisfaction
Employee Salary Hike Percentage
Experience Years In CurrentRole
Employee Enviroment satisfaction: Maximum Number of Employees Performance Rating belongs to EmpEnvironmentSatisfaction Level 3 & Level 4, It contains 367 & 361.

Employee last salary hike percent: More Number of Employees whose salary hike percentage belongs to 11-19 % are getting 2 & 3 performance rating Maximum time. as well asEmployees whose salary hike percentage is in between 20-22%, There performance rating is 4.

Employee work life balance: In EmpWorkLifeBalance, level 3 is showing high Performance Rating of employees

# Goal 3: A Trained model which can predict the employee performance
The trained model is created using the machine learning algorithm as follows with the accuracy score


Random Forest classifier: 92.50% accuracy

# Goal 4: Recommendations to improve the employee performance
The overall employee performance can be achieved by employee environment satisfaction. The company needs to focus more on the employee environment satisfaction. The salary hike will give the boost to the employees to perform well. Promote the employee ervery 6th month Improve Employee's work-life balance this affects the performance rating. While recruiting for HR, consider the female candidates where they perform well compared to male. The development and sales department is having an overall higher performance comparing to rest of the departments. While some of the employees who gives feedback like Low & Medium from Job Satisfaction & Relationship Satisfaction feature, such employees gives Excellent performance more in number. So company should focus on them.
