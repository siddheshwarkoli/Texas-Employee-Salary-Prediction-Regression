# Texas-Employee-Salary-Prediction-Regression

## <b>DOMAIN OVERVIEW
#### <b>DOMAIN: FINANCEC
#### <b>PROBLEM: Predictive model which will help theTexas state government  team to know the payroll information of employees of the state of Texas


## <b>TYPE OF MACHINE LEARNING PROBLEM.
- <b>It is a Regression problem, where given the above set of features, we need to predict payroll information (e.g., salaries) for its employees based on various factors such as job titles, department, employment status, experience, location, and other employee-related information..<br>
#### <b>LIST OF ALGORITHMS USES FOR Regression
<b>
    
- Linear Regression
- KNeighborsRegressor
- DecisionTreeRegressor
- RandomForestRegressor
- GradientBoostingRegressor
- XGBRegressor


### <b>TASK 1
##### <b>PREPARE A COMPLETE DATA ANALYSIS REPORT ON THE GIVEN DATA.
### <b>TASK 2
#### <b>CREATE A PREDICTIVE MODEL WHICH WILL HELP THETEXAS STATE GOVERNMENT  TEAM TO KNOW THE PAYROLL INFORMATION OF EMPLOYEES OF THE STATE OF TEXAS.
### <b>TASK 3
#### <b>1) WHO ARE THE OUTLIERS IN THE SALARIES?
#### <b>2) WHAT DEPARTMENTS/ROLES HAVE THE BIGGEST WAGE DISPARITIES BETWEEN MANAGERS AND EMPLOYEES?
#### <b>3) HAVE SALARIES AND TOTAL COMPENSATIONS FOR SOME ROLES/ DEPARTMENTS/ HEAD-COUNT CHANGED OVER TIME?




## <b>1) INTRODUCTION:
- The Texas Employee Salary Prediction dataset contains information on various employee attributes, including personal details, employment status, and salary-related data.
- The columns include details such as the employee's agency, job title, ethnicity, gender, employment status, hourly rate, hours worked per week, monthly and annual salary, and various flags related to job positions (e.g., multiple jobs, combined salary).
- The dataset is used to predict employee salaries based on factors like job title, hours worked, and employment status, providing insights into salary trends and workforce characteristics within Texas state agencies.
- It can be used for analysis, modeling, or predictive tasks related to employee compensation.


## <b>2) DATASET OVERVIEW

#### <b>Feature	Description
- <b>Age</b><br>Age of the person

- <b>AGENCY</b><br>A business or organization providing a particular serivice on behalf of another business,person,or group.
- <b>AGENCY NAME</b><br>A person or thing through which power is used or something is achieved in this dataset Agency names are given
- <b>LAST NAME</b><br>It is the last name of indivisual/employee record.
- <b>FIRST NAME</b><br>It is the first name of indivisual/employee record.
- <b>MI</b><br>Middle intial is given 
- <b>CLASS CODE</b><br>These codes must be establised before employees can be added to the system and payrolls processed.
- <b>CLASS TITLE</b><br>The official title used for all personnel and payroll processes.
- <b>ETHNICITY</b><br>The quality or fact of belonging to a population group or subgroup made up of people. Here Ethnicity has 6 unique categories White,HISPANIC,BLACK,  ASIAN, OTHER,AM INDIAN,etc. 
- <b>GENDER</b><br>
Is the range of characteristicsRelated to being female or male and recognizing the differences between them.h
- <b>STATUS</b><br>Position or rank in relation to others.
- <b>EMPLOYEE DATE</b><br>Date of joining of an individua/employeel.
- <b>HRLY RATE</b><br>The amount of money that is charged, paid, or earned for every hour worked.
- <b>HRS PER WEEK</b><br>The number of hours in a week that the employee normally would work for the shared work employer or 40 hours.
- <b>MONTHLY</b><br>A salary is the money that someone is paid each month by their employer.
- <b>ANNUAL</b><br>An annual salary is the total amount of money you earn from a job in a year.
- <b>STATE NUMBER</b><br>A unique number assigned to a business or organization by the state where the business operates, and is used for filing taxes and hiring employees.
- <b>DUPLICATED</b><br>One of two or more identical things.
- <b>MUTIPLE FULL TIME JOBS</b><br>Individuals works on one or more jobs in full time.
- <b>COMBINED MULTIPLE JOBS</b><br>The Combine Jobs feature allows you to merge two or more jobs from the same market view into a single job.
- <b>SUMMED ANNUAL SALARY</b><br>Total salary earned by an individual in a year including mutiple full time jobs and combined multiple jobs.
- <b>HIDE FROM SEARCH</b><br>Gives you the option for your web searches to be hidden with respect to organisatio.


## <B>3) PROBLEM UNDERSTANDING
    
- The Texas Employee Salary Prediction problem involves predicting the salaries of employees based on various factors such as job title, hours worked, ethnicity, gender, and employment status.
- The goal is to build a model that accurately predicts annual salaries from available features, enabling insights into salary trends and workforce characteristics across Texas state agencies.
- This can aid in budget planning, policy-making, and understanding compensation patterns.


## <B>4) REPORT ON CHALLENGES FACED
- In this project, we faced several challenges while working with the data and building predictive models. Here’s a detailed report of the challenges.

### <B>A) DATA PREPROCESSING
<B>1) MISSING OR NULL VALUES
- While working on this dataset,In Basic checks was to see if there were any missing or null values in the data. Missing values can negatively impact the performance of machine learning models.

- This dataset had no missing values. If there were any, techniques like imputing missing values using the mean/median for numerical columns or the mode for categorical columns would have been applied.

<B>2) HANDLED DUPLICATE DATA AND CHECKED DATA CURRUPTION
- The dataset was thoroughly checked for duplicates and data corruption, and no duplicates were found.

<B>3) EXTRACTING THE NUMBER OF EXPERIENCE YEARS FROM THE EMPLOY_DATE COLUMN.
- Extracting the number of experience years from the EMPLOY_DATE column posed a challenge due to inconsistent date formats.
- Accurately calculating the tenure required standardizing the dates and handling gaps in employment history, ensuring the derived experience years were reliable for analysis.

### <B>B) PERFORMING EDA (EXPLORATORY DATA ANALYSIS)
- In this dataset we Analyse numerical and catagorial column using various plots and chekcs relation between two features. Also we Analysed Using univariate , Bivariate and multivariate by plotting the graphs and also we mentioned each insights below the graphs.

### <B>C) OUTLIERS HANDLING
- In a Texas Employee Salary Prediction dataset, checking and handling outliers might not be important
- The outliers represent valid data points (e.g., high salaries for senior staff or low salaries for part-time employees), and removing them would lead to a loss of valuable information

### <B>D) CONVERTING CATEGORICAL DATA
- The dataset included categories like Agency_Name,Class_Title,Ethnicity,Gender and Status which machines can't understand directly.
- So we converted these catagories into numerical using encoding technique.
- We used One Hot Encoding

### <B>E) FEATURE SELECTION
- We analyzed the relationships between features using a heatmap. This helped us understand which features were most important for Prediction. which are unwanted
- From heatmap we analyzed that.
    - Monthly is having 0.98 correlation with summed_annual_salary, so both columns are highly co related with each other.
    - Multiple_full_time_jobs is highly correlated with every other feature
    - MONTHLY and ANNUAL columns are highly correlated with each other i.e, 100% so we are dropping MONTHLY columns.
 
### <B>F) SCALING
- Sacling the data is not required for the given dataset because we have only limited or very less variations in the feature columns.

### <B>G) MODEL SELECTION
- We tried different machine learning models for this regression problem:

<B>THE LINEAR REGRESSION MODEL IS CONSIDERED THE BEST MODEL FOR PERFORMANCE BASED ON THE FOLLIWING METRICES:
- R-squared Value:
    - The R-squared value on both the training data (0.9498) and testing data (0.9217) is quite high, indicating that the model explains a significant portion of the variance in the data.
    - Higher R-squared values suggest that the model is performing well.

- This model's strong R-squared values and relatively low MAE, MSE, and RMSE suggest it is performing well, making linear regression a good choice for Texas Employee Salary Predictions.


### <B>H) MODEL DEPLOYMENT
- Once the model was trained and evaluated, we saved the model using pickle.
- This allows us to load the model and make predictions on new, unseen data without retraining the model each time.

### <b>I) RESULT
| Model                               | Train R² Score | Test R² Score |
| ----------------------------------- | -------------- | ------------- |
| Linear Regression                   | 0.9497         | 0.9217        |
| Decision Tree Regressor             | 1.0000         | 0.8174        |
| Random Forest Regressor             | 0.9792         | 0.8712        |
| K-Nearest Neighbors (KNN) Regressor | 0.2565         | 0.0364        |
| XGBoost                             | 0.8567         | 0.8328        |
| Gradient Boosting Regressor         | 0.6630         | 0.6468        |



#### <b>RESULT SUMMARY
<b>

- Linear Regression has R-squared Value: The R-squared value on both the training data (0.9497) and testing data (0.9217) is quite high, indicating that the model explains a significant portion of the variance in the data. Higher R-squared values suggest that the model is performing well.

- Decision Tree Regressor Model has The perfect R² on the training set (1.0) combined with a lower R² on the test set (0.8174) suggests overfitting. This means the model has memorized the training data rather than learning the general patterns

- Random Forest The model explains 0.9792 of the variance in the training data, indicating that the model fits the training data very well but the model explains 0.8712 of the variance in the test data which seems that overfitting.

- Gradient Boosting Regressor The model explains 0.6630 of the variance in the training data. and The model explains 0.6468 of the variance in the test data.which seems generalizaed but very less R2 score. This indicates that the model fits the training data moderately well but doesn't capture all patterns perfectly.

- XGBoost has The drop from 0.8567 (training) to 0.8328 (test) is relatively small it has best r2 score as compared to linear regression its less.


### <B>J) CONCLUSION
- By comparing various regression machine learning models,we found that Linear Regression model is best suited for Texas Salary Prediction Dataset
- This dataset offers a wealth of information that can be used for various analytical and predictive tasks related to employee salary predictions.
- It is possible to generate meaningful insights into factors that influence salaries, identify potential salary disparities, and build models to predict compensation based on job classification, experience, and demographics.
- Proper handling of potential data quality issues, such as duplicates and privacy flags, is crucial to ensure accurate and ethical analysis

- K-Nearest Neighbors (KNR) This model has very low R² values on both the training (0.2565) and test (0.0364) sets, indicating that it doesn't explain much of the variance in the data and is underfitting the model.

# <b>You and Copy this but give a Star as a Compliment
# <B>THANK YOU

# <b>END OF PROJECT
<b>SIDDHESHWAR KOLI<br>
<b>ANY QUERY CONTACT : siddheshwarkoli10@gmail.com

