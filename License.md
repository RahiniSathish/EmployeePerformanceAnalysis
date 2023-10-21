
# Employee Performance Analysis

This repository contains a data science project focused on analyzing and improving employee performance at INX Future Inc, a leading data analytics and automation solutions provider. The project aims to provide actionable insights into employee performance and recommendations to enhance it while maintaining a positive work environment.

Project Structure
Project Summary:

Requirement: Data from third-party sources.
Analysis: Interpreting data and summary of various choices, from selecting machine learning algorithms to data processing techniques.
Summary: Project summary with analysis and recommendations.
data:

external: Data from third-party sources.
processed: The final, canonical data sets for modeling.
raw: The original, immutable data dump.
src:

Data Processing: Jupyter notebooks for data processing, data munging, and exploratory analysis.
data_processing.ipynb
data_exploratory_analysis.ipynb
models: Scripts to train machine learning models and make predictions.
train_model.ipynb
predict_model.ipynb
visualization: Scripts for creating exploratory and results visualizations.
visualize.ipynb
references: Data dictionaries, manuals, and explanatory materials.

Getting Started
Data: Obtain the project data from INX_Future_Inc_Employee_Performance_CDS_Project2_Data_V1.8.xls and place it in the appropriate data directories (external, processed, or raw) as needed.

Data Processing: Explore and process the data using the Jupyter notebooks provided in the src/Data Processing directory.

Model Training: Use the scripts in the src/models directory to train machine learning models based on the processed data.

Predictions: Run the predict_model.ipynb script to make predictions using the trained model.

Visualization: Generate visualizations using the visualize.ipynb script.

Summary and Recommendations: Refer to the Project Summary/Summary section for a comprehensive project summary with analysis and recommendations.

Contributing
We welcome contributions to this project. If you have suggestions or improvements to share, please submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
We thank INX Future Inc for providing the data and supporting this analysis.
The project structure was inspired by the best practices for organizing data science projects.

## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Documentation

[Documentation](https://linktodocumentation)


## Task
The Goal and Insights of the project are as follows:
Department wise performances
Top 3 Important Factors effecting employee performance
A trained model which can predict the employee performance based on factors as inputs. This will be used to hire employees Recommendations to improve the employee performance based on insights from analysis The given Employee dataset consist of 1200 rows. The features present in the data are 28 columns. The shape of the dataset is 1200x28. The 28 features are classified into quantitative and qualitative where 19 features are quantitative (11 columns consists numeric data & 8 columns consists ordinal data) and 8 features are qualitative. EmpNumber consist alphanumerical data (distinct values) which doesn't play a role as a relevant feature for performance rating.

From Correlation we can get the important aspects of the data, Correlation between features and Performance Rating.Correlation is a statistical measure that expresses the extent to which two variables are linearly related.The analysis of the project has gone through the stage of Univariate,Bivariate & Multivariate analysis, correlation analysis and analysis by each department to satisfy the project goal.

The dataset consists of Categorical data and Numerical data. The Target variable consist of ordinal data, so this is a classification problem.The multiple machine learning model used in this project is Support vector classifier, Random forest classifier & Artifical neural network[Multilayer percepton]. from above all models Artifical neural network[Multilayer percepton] predicts higher accuracy 95.80%.

One of the important goal of this project is to find the important feature affecting the performance rating. The important features were predicted using the machine learning model feature importance technique. The main technique used in the preprocessing data using the Mannual & Frequency encoding method to convert the string - categorical data into numerical data, because, Most of machine learning methods are based on numerical methods where strings are not supportive. The overall project was performed and achieved the goals by using the machine learning model and visualization techniques.

1. Requirement
The data was given from the IABAC for this project where the collected source is IABAC™. The data is based on INX Future Inc, (referred as INX ). It is one of the leading data analytics and automation solutions provider with over 15 years of global business presence. INX is consistently rated as top 20 best employers past 5 years. The data is not from the real organization. The whole project was done in Jupiter notebook with python platform.

2. Analysis
Data were analyzed by describing the features present in the data. the features play the bigger part in the analysis. The features tell the relation between the dependent and independent variables. Pandas also help to describe the datasets answering following questions early in our project. The data present in the dataset are divided into numerical and categorical data.

Categorical Features EmpNumber Gender EducationBackground MaritalStatus EmpDepartment EmpJobRole BusinessTravelFrequency OverTime Attrition

Numerical Features Age DistanceFromHome EmpHourlyRate NumCompaniesWorked EmpLastSalaryHikePercent TotalWorkExperienceInYears TrainingTimesLastYear ExperienceYearsAtThisCompany ExperienceYearsInCurrentRole YearsSinceLastPromotion YearsWithCurrManager

Ordinal Features EmpEducationLevel EmpEnvironmentSatisfaction EmpJobInvolvement EmpJobLevel EmpJobSatisfaction EmpRelationshipSatisfaction EmpWorkLifeBalance PerformanceRating

3.Univariate, Bivariate & Multivariate Analysis
Library Used: Matplotlib & Seaborn
Plots Used: Histplot, Lineplot, CountPlot, Barplot
Tip: All Observation or insights written below the plots
Univariate Analysis: In univariate analysis we get the unique labels of categorical features, as well as get the range & density of numbers

Bivariate Analysis: In bivariate analysis we check the feature relationship with target veriable.

Multivariate Analysis: In multivariate Analysis check the relationship between two veriable with respect to the target veriable.

CONCLUSION There are some features are positively correlated with performance rating( Target variable) [Emp Environment Satisfaction,Emp Last Salary Hike Percent,Emp Work Life Balance]

4.Explotary Data Analysis
Basic Check & Statistical Measures* Their is no constant column is present in Numerical as well as categoriacl data.

Distribution of Continuous Features:
In general, one of the first few steps in exploring the data would be to have a rough idea of how the features are distributed with one another. To do so, we shall invoke the familiar distplot function from the Seaborn plotting library. The distribution has been done by both numerical features. it will show the overall idea about the density and majority of data present in a different level.

The age distribution is starting from 18 to 60 where the most of the employees are laying between 30 to 40 age count Employees are worked in the multiple companies up to 8 companies where most of the employees worked up to 2 companies before getting to work here. The hourly rate range is 65 to 95 for majority employees work in this company. In General, Most of Employees work up to 5 years in this company. Most of the employees get 11% to 15% of salary hike in this company.

Check Skewness and Kurtosis of Numerical Features
Checking weather the data is Normally distributed or Not with Skewness and Kurtosis**
YearsSinceLastPromotion, This column is skewed
skewness for YearsSinceLastPromotion: 1.9724620367914252
kurtosis for YearsSinceLastPromotion: 3.5193552691799805
Distribution of Mean of Data
Distribution of mean close to guassian distribution with mean value 9.5
we can say that around 80% feature mean lies between 8.5 to 10.5
Distribution of Standard Deviation of Data
Distribution of standard deviation of data also look like guassian distribution around 30% of feature standard deviation around the range of 3 3 to 20 and remaining 70% feature standard deviation in between 0 to 2
5.Data Pre-Processing
Check Missing Value: Their is no missing value in data

Categorical Data Conversion: Handel categorical data with the help of frequency and mannual encoding, because feature is contain lot's of labels

Mannual Encoding: Mannual encoding is a best techinque to handel categorical feature with the help of map function, map the labels based on frequency.

Frequency Encoding: Frequency encoding is an encoding technique to transform an original categorical variable to a numerical variable by considering the frequency distribution of the data getting value counts.

Outlier Handling Some features are contain outliers so we are impute this outlier with the help of IQR because in all features data is not normally distributed

Feature Transformation: In YearsSinceLastPromotion some skewed & kurtosis is present, so we are use Square Root Transformation techinque

Square root transformation: Square root transformation is one of the many types of standard transformations.This transformation is used for count data (data that follow a Poisson distribution) or small whole numbers. Each data point is replaced by its square root. Negative data is converted to positive by adding a constant, and then transformed.
Q-Q Plot: Q–Q plot is a probability plot, a graphical method for comparing two probability distributions by plotting their quantiles against each other.
Scaling The Data: scaling the data with the help of Standard scalar
Standard Scaling: Standardization is the process of scaling the feature, it assumes the feature follow normal distribution and scale the feature between mean and standard deviation, here mean is 0 and standard deviation is always 1.
6.Future Selection
Drop unique and constant feature: Dropping employee number because this is a constant column as well as drop Years Since Last Promotion because we create a new feaure using square root transformation

Checking Correlation: Checking correlation with the help of heat map, and get the their is no highly correlated feature is present.

Heatmap: A heatmap is a graphical representation of data that uses a system of color-coding to represent different values.

Check Duplicates: In this data Their is no dupicates is present.

PCA: Use pca to reduce the dimension of data, Data is contain total 27 feature after dropping unique and constant column,from PCA it shows the 25 feature has less varaince loss, so we are going to select 25 feature.

Principal component analysis (PCA) is a popular technique for analyzing large datasets containing a high number of dimensions/features per observation, increasing the interpretability of data while preserving the maximum amount of information, and enabling the visualization of multidimensional data. Formally, PCA is a statistical technique for reducing the dimensionality of a dataset.

Saving Pre-Process Data: save the all preprocess data in new file and add target feature to it.
7.Machine learning Model Creation & Evaluation
Define Dependant and Independant Features:

Balancing the data: The data is imbalance, so we need to balance the data with the help of SMOTE

SMOTE: SMOTE (synthetic minority oversampling technique) is one of the most commonly used oversampling methods to solve the imbalance problem. It aims to balance class distribution by randomly increasing minority class examples by replicating them. SMOTE synthesises new minority instances between existing minority instances. 3.Splitting Training And Testing Data: 80% data use for training & 20% data used for testing

Algorithm:
AIM: Create a sweet spot model (Low bias, Low variance)
HERE WE WILL BE EXPERIMENTING WITH THREE ALGORITHM

Support Vector Machine
Random Forest
Artificial Neural Network [MLP Classifier]
Support vector machine well perform on training data with accuracy 96.61% but the test score is 94.66 after applying Hyperparameter tunning score is 98.28 means model is overfit.
Random forest very well perform in training data with 100% accuracy but in testing 95.61% after doing hyperparameter tunning testing score is decreases.
Artifical neural network[Multilayer percepton] perform very well on training data with 98.95% accuracy and testing score is 95.80%. So we are select Artifical neuranl network [Multilayer percepton] model.
8.Saving Model
Save model with the helpof pickle file

Tools and Library Used:
Tools:
Jupyter

Library Used:
Pandas Numpy Matplotlib Seaborn pylab Scipy Sklearn Pickle

Goal 1: Department Wise Performances
PLOT USED

Violinplot: It shows the distribution of quantitative data across several levels of one (or more) categorical variables such that those distributions can be compared.
CountPlot: countplot is used to Show the counts of observations in each categorical bin using bars. Sales: The Performace rating level 3 is more in the sales department. The male performance rating the little bit higher compared to female.
Human Resources: The majority of the employees lying under the level 3 performance . The older people are performing low in this department. The female employees in HR department doing really well in their performance.

Development: The maximum number of employees are level 3 performers. Employees of all age are performing at the level of 3 only. The gender-based performance is nearly same for both.

Data Science: The highest average of level 3 performance is in data science department. Data science is the only department where less number of level 2 performers. The overall performance is higher compared to all departments. Male employees are doing good in this department.

Research & Development: The age factor is not deviating from the level of performance here where different employees with different age are there in every level of performance. The R&D has the good female employees in their performance.

Finance: The finance department performance is exponentially decreasing when age increases. The male employees are doing good. The experience factor is inversely relating to the performance level.

Goal 2: Top 3 Important Factors effecting employee performance
The top three important features affecting the performance rating are ordered with their importance level as follows,

Employment Environment Satisfaction
Employee Salary Hike Percentage
Experience Years In CurrentRole
Employee Enviroment satisfaction: Maximum Number of Employees Performance Rating belongs to EmpEnvironmentSatisfaction Level 3 & Level 4, It contains 367 & 361.

Employee last salary hike percent: More Number of Employees whose salary hike percentage belongs to 11-19 % are getting 2 & 3 performance rating Maximum time. as well asEmployees whose salary hike percentage is in between 20-22%, There performance rating is 4.

Employee work life balance: In EmpWorkLifeBalance, level 3 is showing high Performance Rating of employees

Goal 3: A Trained model which can predict the employee performance
The trained model is created using the machine learning algorithm as follows with the accuracy score


Random Forest classifier: 95.61% accuracy

Goal 4: Recommendations to improve the employee performance
The overall employee performance can be achieved by employee environment satisfaction. The company needs to focus more on the employee environment satisfaction. The salary hike will give the boost to the employees to perform well. Promote the employee ervery 6th month Improve Employee's work-life balance this affects the performance rating. While recruiting for HR, consider the female candidates where they perform well compared to male. The development and sales department is having an overall higher performance comparing to rest of the departments. While some of the employees who gives feedback like Low & Medium from Job Satisfaction & Relationship Satisfaction feature, such employees gives Excellent performance more in number. So company should focus on them.## Color Reference

| Color             | Hex                                                                |
| ----------------- | ------------------------------------------------------------------ |
| Example Color | ![#0a192f](https://via.placeholder.com/10/0a192f?text=+) #0a192f |
| Example Color | ![#f8f8f8](https://via.placeholder.com/10/f8f8f8?text=+) #f8f8f8 |
| Example Color | ![#00b48a](https://via.placeholder.com/10/00b48a?text=+) #00b48a |
| Example Color | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) #00d1a0 |


## License
      Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
      outstanding shares, or (iii) beneficial ownership of such entity.

      "You" (or "Your") shall mean an individual or Legal Entity
      exercising permissions granted by this License.

      "Source" form shall mean the preferred form for making modifications,
      including but not limited to software source code, documentation
      source, and configuration files.

      "Object" form shall mean any form resulting from mechanical
      transformation or translation of a Source form, including but
      not limited to compiled object code, generated documentation,
      and conversions to other media types.

      "Work" shall mean the work of authorship, whether in Source or
      Object form, made available under the License, as indicated by a
      copyright notice that is included in or attached to the work
      (an example is provided in the Appendix below).

      "Derivative Works" shall mean any work, whether in Source or Object
      form, that is based on (or derived from) the Work and for which the
      editorial revisions, annotations, elaborations, or other modifications
      represent, as a whole, an original work of authorship. For the purposes
      of this License, Derivative Works shall not include works that remain
      separable from, or merely link (or bind by name) to the interfaces of,
      the Work and Derivative Works thereof.

      "Contribution" shall mean any work of authorship, including
      the original version of the Work and any modifications or additions
      to that Work or Derivative Works thereof, that is intentionally
      submitted to Licensor for inclusion in the Work by the copyright owner
      or by an individual or Legal Entity authorized to submit on behalf of
      the copyright owner. For the purposes of this definition, "submitted"
      means any form of electronic, verbal, or written communication sent
      to the Licensor or its representatives, including but not limited to
      communication on electronic mailing lists, source code control systems,
      and issue tracking systems that are managed by, or on behalf of, the
      Licensor for the purpose of discussing and improving the Work, but
      excluding communication that is conspicuously marked or otherwise
      designated in writing by the copyright owner as "Not a Contribution."

      "Contributor" shall mean Licensor and any individual or Legal Entity
      on behalf of whom a Contribution has been received by Licensor and
      subsequently incorporated within the Work.

   2. Grant of Copyright License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      copyright license to reproduce, prepare Derivative Works of,
      publicly display, publicly perform, sublicense, and distribute the
      Work and such Derivative Works in Source or Object form.

   3. Grant of Patent License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      (except as stated in this section) patent license to make, have made,
      use, offer to sell, sell, import, and otherwise transfer the Work,
      where such license applies only to those patent claims licensable
      by such Contributor that are necessarily infringed by their
      Contribution(s) alone or by combination of their Contribution(s)
      with the Work to which such Contribution(s) was submitted. If You
      institute patent litigation against any entity (including a
      cross-claim or counterclaim in a lawsuit) alleging that the Work
      or a Contribution incorporated within the Work constitutes direct
      or contributory patent infringement, then any patent licenses
      granted to You under this License for that Work shall terminate
      as of the date such litigation is filed.

   4. Redistribution. You may reproduce and distribute copies of the
      Work or Derivative Works thereof in any medium, with or without
      modifications, and in Source or Object form, provided that You
      meet the following conditions:

      (a) You must give any other recipients of the Work or
          Derivative Works a copy of this License; and

      (b) You must cause any modified files to carry prominent notices
          stating that You changed the files; and

      (c) You must retain, in the Source form of any Derivative Works
          that You distribute, all copyright, patent, trademark, and
          attribution notices from the Source form of the Work,
          excluding those notices that do not pertain to any part of
          the Derivative Works; and

      (d) If the Work includes a "NOTICE" text file as part of its
          distribution, then any Derivative Works that You distribute must
          include a readable copy of the attribution notices contained
          within such NOTICE file, excluding those notices that do not
          pertain to any part of the Derivative Works, in at least one
          of the following places: within a NOTICE text file distributed
          as part of the Derivative Works; within the Source form or
          documentation, if provided along with the Derivative Works; or,
          within a display generated by the Derivative Works, if and
          wherever such third-party notices normally appear. The contents
          of the NOTICE file are for informational purposes only and
          do not modify the License. You may add Your own attribution
          notices within Derivative Works that You distribute, alongside
          or as an addendum to the NOTICE text from the Work, provided
          that such additional attribution notices cannot be construed
          as modifying the License.

      You may add Your own copyright statement to Your modifications and
      may provide additional or different license terms and conditions
      for use, reproduction, or distribution of Your modifications, or
      for any such Derivative Works as a whole, provided Your use,
      reproduction, and distribution of the Work otherwise complies with
      the conditions stated in this License.

   5. Submission of Contributions. Unless You explicitly state otherwise,
      any Contribution intentionally submitted for inclusion in the Work
      by You to the Licensor shall be under the terms and conditions of
      this License, without any additional terms or conditions.
      Notwithstanding the above, nothing herein shall supersede or modify
      the terms of any separate license agreement you may have executed
      with Licensor regarding such Contributions.

   6. Trademarks. This License does not grant permission to use the trade
      names, trademarks, service marks, or product names of the Licensor,
      except as required for reasonable and customary use in describing the
      origin of the Work and reproducing the content of the NOTICE file.

   7. Disclaimer of Warranty. Unless required by applicable law or
      agreed to in writing, Licensor provides the Work (and each
      Contributor provides its Contributions) on an "AS IS" BASIS,
      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
      implied, including, without limitation, any warranties or conditions
      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
      PARTICULAR PURPOSE. You are solely responsible for determining the
      appropriateness of using or redistributing the Work and assume any
      risks associated with Your exercise of permissions under this License.

   8. Limitation of Liability. In no event and under no legal theory,
      whether in tort (including negligence), contract, or otherwise,
      unless required by applicable law (such as deliberate and grossly
      negligent acts) or agreed to in writing, shall any Contributor be
      liable to You for damages, including any direct, indirect, special,
      incidental, or consequential damages of any character arising as a
      result of this License or out of the use or inability to use the
      Work (including but not limited to damages for loss of goodwill,
      work stoppage, computer failure or malfunction, or any and all
      other commercial damages or losses), even if such Contributor
      has been advised of the possibility of such damages.

   9. Accepting Warranty or Additional Liability. While redistributing
      the Work or Derivative Works thereof, You may choose to offer,
      and charge a fee for, acceptance of support, warranty, indemnity,
      or other liability obligations and/or rights consistent with this
      License. However, in accepting such obligations, You may act only
      on Your own behalf and on Your sole responsibility, not on behalf
      of any other Contributor, and only if You agree to indemnify,
      defend, and hold each Contributor harmless for any liability
      incurred by, or claims asserted against, such Contributor by reason
      of your accepting any such warranty or additional liability.

   END OF TERMS AND CONDITIONS

   APPENDIX: How to apply the Apache License to your work.

      To apply the Apache License to your work, attach the following
      boilerplate notice, with the fields enclosed by brackets "[]"
      replaced with your own identifying information. (Don't include
      the brackets!)  The text should be enclosed in the appropriate
      comment syntax for the file format. We also recommend that a
      file or class name and description of purpose be included on the
      same "printed page" as the copyright notice for easier
      identification within third-party archives.

   Copyright [yyyy] [name of copyright owner]

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
