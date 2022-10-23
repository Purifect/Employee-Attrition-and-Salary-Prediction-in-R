
# Employee Attrition and Salary Prediction in R

**Contributor**: [**Puri Rudick**](https://www.github.com/Purifect)

Talent management is defined as the iterative process of developing and retaining employees. It may include workforce planning, employee training programs, identifying high-potential employees and reducing/preventing voluntary employee turnover (attrition).

This project aims to leverage data science for talent management. The objectives of this project are:
    
- Provide job role specific insights that exist in the data set.
- Identify top factors that contribute to turnover and create a classification model to predict employee attrition.
- Build a regression model to predict employee's monthly income which proved to be one of the tops factors contribute to turnover.

**Results**:
- For the top factors for attrition, I created dynamic visualization using an **RShiny** app to help visualization the dataset: https://purifect.shinyapps.io/Employee_Attrition/
- For employee attrition classification model, I used **K-Nearest Neighbors (KNN) algorithm**.  The model achieved the **accuracy of 86.7%** with the 95% CI of Accuracy of (83.7%, 89.3%).
- For employee's monthly income, I used **Multiple Linear Regression (MLR) model**.  The model's **Adjusted R2 is 0.9102** with **RSME of $1,035.80**.

## :star2: Deliverables :star2:

Below are my deliverable links of RShiny app, video presentation, PowerPoint, and full analysis (in both R Markdown and HTML files).

- [RShiny](https://purifect.shinyapps.io/Employee_Attrition/)
- [YouTube - Video Presentation](https://youtu.be/NcQwkyrFcz0)
- [PowerPoint Presentation](https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/CaseStudy2_Puri%20Rudick.pptx)
- Full Analysis: [R Markdown](https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/CaseStudy2_Attrition.Rmd), [HTML](https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/CaseStudy2_Attrition.Rmd)

---

## Table of Contents
- [Data Description](#P1)
- [Job Role Specific Insights](#P2)
- [Employee Attrition Classification Model Using KNN](#P3)
- [Employee's Monthly Income Prediction Model Using MLR](#P4)
- [Conclusions](#P5)

---

<a name="P1"></a>

## Data Description

**Train Dataset**

- The dataset contains **870 observations** (employees) with **36 variables**.
- **Imbalanced target** variable:
  - 140 observations were identified as ‘Attrition'
  - 730 observations were identified as ’No Attrition’.
- The dataset has **no missing values**.
- **The dataset was spitted into 70% Train Set and 30% Validation Set before fitting the models.** 

**Test dataset** contains 300 observations.

[Back to Top](#BackToTop)

---

<a name="P2"></a>

## Job Role Specific Insights
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/JobRole_vsAttrition.png?raw=true" style="center" width="500"/>
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/Trends_byJobRole.png?raw=true" style="center" width="500"/>

*(Top) Bar Chart Displays Percent Attrition in Each Job Role.*<br>
*(Bottom) Spider Plot Displays Satisfaction and Wokr Life Balance (WLB) for Each Job Role.*

- Job roles with high percentage of attrition are: Sale Representative, Human Resources, and Laboratory Technician.
- Higher job levels, like Director and Manager, have low percentage of attrition.
- Manufacturing Directors have highest  Environment Satisfaction, while Healthcare Representative have highest Job Satisfaction, and Human Resources have highest Work Life Balance.

[Back to Top](#BackToTop)


---
<a name="P3"></a>

## Employee Attrition Classification Model Using KNN
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/KNN_Summary.png?raw=true" style="center" width="700"/>

With K = 21, the model achieved the **accuracy of 86.7%** with the 95% CI of Accuracy of (83.7%, 89.3%).

[Back to Top](#BackToTop)

---
<a name="P4"></a>

## Employee's Monthly Income Prediction Model Using MLR

Before fitting the MLR Model, I looked at the correlation coefficient with p-value between all numerical variables.
I found that there are 7 columns that have statistically significant correlation (p-value < .05) with good range of correlation coefficient which are Age, JobLevel, TotalWorkingYears, YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager.

<img src="https://github.com/Purifect/Employee-Attrition-and-Salary-Prediction-in-R/blob/main/photos/Variable_Corr2.png?raw=true" style="center" width="500"/>

When included all 7 variables to the linear regression model, only JobLevel and TotalWorkingYears are significant.
The categorical variables then added to the MLR model, none of them makes the model better and/or makes the p-value statistically significant.
So, I decided to use only JobLevel, TotalWorkingYears, YearsWithCurrManager for MLR model.  The MLR model summary as shown below.

<img src="https://github.com/Purifect/Employee-Attrition-and-Salary-Prediction-in-R/blob/main/photos/MLR_Summary.png?raw=true" style="center" width="700"/>

 The plots below had run to help to check fir MLR assumptions:
 - Normality – Residuals of the linear model is assumed to be normally distributed
 - Equal Variance – The variance of the residuals is constant for every combination of independent variables and thus constant across all the predicted values (residual plots)
 - Independence – Observations are identically and independently distributed (i.i.d.)
 
 <img src="https://github.com/Purifect/Employee-Attrition-and-Salary-Prediction-in-R/blob/main/photos/MLR_Assumptions.png?raw=true" style="center" width="500"/>


[Back to Top](#BackToTop)

---
<a name="P5"></a>

## Conclusions

- - For the top factors for attrition, I created dynamic visualization using an **RShiny** app to help visualization the dataset: https://purifect.shinyapps.io/Employee_Attrition/
- For employee attrition classification model, I used **K-Nearest Neighbors (KNN) algorithm**.  The model achieved the **accuracy of 86.7%** with the 95% CI of Accuracy of (83.7%, 89.3%).
- For employee's monthly income, I used **Multiple Linear Regression (MLR) model**.  The model's **Adjusted R2 is 0.9102** with **RSME of $1,035.80**.


[Back to Top](#BackToTop)

---
