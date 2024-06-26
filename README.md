# Forecasting Employee turnover

## Purpose
To develop an employee retention model for Flux Motors by analyzing data and identifying key factors that influence an employee's decision to leave the company. This model will predict the likelihood of an employee's departure, enabling the formulation of targeted employee engagement strategies tailored to those at high risk of attrition. Ultimately, the goal is to increase overall employee retention rates through proactive interventions and initiatives


## 🔗 Links

### Dashboard Link : [HR Analytics Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYzAyNGUzZTgtMWY4OC00MTliLTljNDktMzBmOTQ2ZmYzMTBjIiwidCI6IjYwODIzNDA4LTBlYjktNGE0Zi04ZTcxLTY2MzcwYThmNjU4NSJ9&pageName=dcccf17ee4ecb733a9e2)

### Kaggle Notebook For more details: [Click Here To Visit Kaggle Notebbok](https://www.kaggle.com/code/subhrayansamajdar/forecasting-employee-turnover-dt-rf-xgb?scriptVersionId=182742824)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subhrayan-samajdar-78b17b132?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BKT08BcH3SnWhaOJFAjaQ1w%3D%3D)


[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://subhrayan.github.io/)





## PROJECT OVERVIEW

Flux Motors faces a high employee turnover rate, which concerns the senior leadership due to the significant costs associated with recruiting, training, and upskilling new employees. To address this challenge, the key factors driving employee turnover should be analyzed. Additionally, it is recommended to determine potential employee departures based on factors such as job title, department, number of projects, average monthly hours, and other relevant data points. This analysis will help the company increase retention and job satisfaction for current employees while saving costs associated with training new hires. The HR team has conducted a survey to acquire employee data, which now needs to be analyzed and used to provide data-driven suggestions to counter the high turnover issue.

### Problem
High rate of turnover among Flux Motors employees, which is very costly. Flux Motors employees are leaving the company more often and are manifesting job dissatisfaction.\ Question to be answered: What's likely to make the employee leave the company?

### Response
Since the variable to be predicted is categorical, a logistic regression or tree-based machine learning model will be used.

### Impact
The model will help predict employee departure and the factors that causes it. The HR can also devise a plan to prevent departures and improve employee retention

### Data source
- The employees survey data is stored in a single CSV file. It can be accessed through - https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction/data

- The dataset possesses the qualities of 'ROCCC'.

### Steps followed 

- step 1 : Data cleaning - Rename columns, addressing missing values, addressing duplicates, addressing outliers
- Step 2 : Exploration and descriptive analysis through EDA
- Step 3 : Building a Logistic regression regression model
- Step 4 : Feature engineering for Logistic regression model
- Step 5 : Building a machine learning models (Random Forest, DecisionTreeClassifier and XGBoost) 
- Step 6 : Feature engineering for ML models
- Step 7 : Modeling Random Forest
- Step 8 : Modeling DecisionTree Classifier
- Step 9 : Modeling XGBoost
- Step 10 : Loading data to Power Bi
- Step 11 : Building Dashboard

## Key Insights 
1. 
 ![newplot (3)](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/45b14e0d-4ee0-42bb-ad3b-42dec7a46450)

![newplot](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/c640fbec-d48f-4c95-9a35-97416469b79a)

There are two groups of employees who left the company: (A) those who worked considerably less than their peers with the same number of projects, and (B) those who worked much more. Of those in group A, it's possible that they were fired. It's also possible that this group includes employees who had already given their notice and were assigned fewer hours because they were already on their way out the door. For those in group B, it's reasonable to infer that they probably quit. The folks in group B likely contributed a lot to the projects they worked in; they might have been the largest contributors to their projects.

   The optimal number of projects for employees to work on seems to be 3–4. The ratio of left/stayed is very small for these cohorts. And aside from the employees who worked on two projects, every group—even those who didn't leave the company—worked considerably more hours than this. It seems that employees here are overworked.

 All employees(145)  with 7 projects did leave.
 
2. 
 ![newplot (1)](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/1a7adb02-4713-4aa6-9deb-1ef966d61499)

The scatterplot above shows that there was a sizeable group of employees who worked ~240–315 hours per month. 315 hours per month is over 75 hours per week for a whole year. It's likely this is related to their satisfaction levels being close to zero.

   The plot also shows another group of people who left, those who had more normal working hours. Even so, their satisfaction was only around 0.4. It's difficult to speculate about why they might have left. It's possible they felt pressured to work more, considering so many of their peers worked more. And that pressure could have lowered their satisfaction levels.

Finally, there is a group who worked ~210–280 hours per month, and they had satisfaction levels ranging ~0.7–0.9.

Note the strange shape of the distributions here. This is indicative of data manipulation or synthetic data.

3. 
![newplot (2)](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/7dbc6ebd-f386-4574-a512-173aaf2203a8)

Employees who left fall into two general categories: dissatisfied employees with shorter tenures and very satisfied employees with medium-length tenures.

   Four-year employees who left seem to have an unusually low satisfaction level. It's worth investigating changes to company policy that might have affected people specifically at the four-year mark, if possible.

   The longest-tenured employees didn't leave. Their satisfaction levels aligned with those of newer employees who stayed

   The histogram shows that there are relatively few longer-tenured employees. It's possible that they're the higher-ranking, higher-paid employees.

4.  
![Screenshot 2024-06-13 012412](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/f8ca49e3-1ffb-4b92-a8f0-5e62d4eda028)

The mean and median satisfaction scores of employees who left are lower than those of employees who stayed. Interestingly, among employees who stayed, the mean satisfaction score appears to be slightly below the median score. This indicates that satisfaction levels among those who stayed might be skewed to the left.

5. 
![newplot (5)](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/bd9371f9-a0c1-4b81-b1dc-07a1e516efd9)

The scatterplot indicates two groups of employees who left: overworked employees who performed very well and employees who worked slightly under the nominal monthly average of 166.67 hours with lower evaluation scores.

   There seems to be a correlation between hours worked and evaluation score.

   Most of the employees in this company work well over 167 hours per month.

6. 
![newplot (6)](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/a19e3e24-d93d-425f-ac6d-8200f10ba5bd)

Very few employees who were promoted in the last five years left.

very few employees who worked the most hours were promoted.

all of the employees who left were working the longest hours.

7. 
![newplot (7)](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/13b9956c-06d5-401c-bd73-204b5b7a38ce)


The correlation heatmap confirms that the number of projects, monthly hours, and evaluation scores all have some positive correlation with each other, and whether an employee leaves is negatively correlated with their satisfaction level.

8. Confusion matrix from Logistic regression model

![Screenshot 2024-06-13 014249](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/408e53d0-f666-42fb-87b5-6c29c5474ef3)

The classification report shows that the logistic regression model achieved a precision of 79%, recall of 82%, f1-score of 80% (all weighted averages), and accuracy of 82%. However, if it's most important to predict employees who leave, then the scores are significantly lower.

Our goal is minimize False negatives: The number of people who left that the model inaccurately predicted did not leave

9. Confusion matrix from Random Forest model after feature engineering and hyperparameter tuning

![Screenshot 2024-06-13 015339](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/fe5dfc9b-0423-4c3f-935f-cedfde3d9f8d)

![Screenshot 2024-06-13 020624](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/d9eaa940-e106-46a1-872e-9809bd02fb48)


The model predicts more false positives than false negatives, which means that some employees may be identified as at risk of quitting or getting fired, when that's actually not the case. But this is still a strong model.

10.  Confusion matrix from XGBoost model

![Screenshot 2024-06-13 020215](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/0933a4d3-5136-4dee-b814-7463e28bd859)

![Screenshot 2024-06-13 020442](https://github.com/Subhrayan/Forecasting-Employee-turnover/assets/154826702/ee38b925-8b43-483f-bbf9-e1fcd701d0b9)


**To retain employees, the following recommendations could be presented to the stakeholders:**

- Cap the number of projects that employees can work on.
- Consider promoting employees who have been with the company for atleast four years, or conduct further investigation about why four-year tenured employees are so dissatisfied.
- Either reward employees for working longer hours, or don't require them to do so.
- High evaluation scores should not be reserved for employees who work 200+ hours per month. Consider a proportionate scale for rewarding employees who contribute more/put in more effort.





