
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
- 
 
Below are my deliverable links of video presentation, PowerPoint, and full analysis (in both R Markdown and HTML files).

- [YouTube - Video Presentation](https://youtu.be/NcQwkyrFcz0)
- [PowerPoint Presentation](https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/CaseStudy2_Puri%20Rudick.pptx)
- Full Analysis: [R Markdown](https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/CaseStudy2_Attrition.Rmd), [HTML](https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/CaseStudy2_Attrition.Rmd)

---

## Table of Contents
- [Data Description](#P1)
- [Job Role Specific Insights](#P2)
- [Employee Attrition Classification Model Using KNN](#P3)
- [Employee's Monthly Income Prediction Using MLR](#P4)
- [References](#References)

---

<a name="P1"></a>

## Data Description

**Train Dataset**

- The dataset contains **870 observations** (employees) with **36 variables**.
- **Imbalanced target** variable:
  - 140 observations were identified as ‘Attrition'
  - 730 observations were identified as ’No Attrition’.
- The dataset has **no missing values**.

**Test dataset** contains 300 observations.

[Back to Top](#BackToTop)

---

<a name="P2"></a>

## Job Role Specific Insights
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/JobRole_vsAttrition.png?raw=true" style="left" width="450"/>
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/Trends_byJobRole.png?raw=true" style="left" width="400"/>

*(Left) Bar Chart Displays Percent Attrition in Each Job Role.*<br>
*(Right) Spider Plot Displays Satisfaction and Wokr Life Balance (WLB) for Each Job Role.*

- Job roles with high percentage of attrition are: Sale Representative, Human Resources, and Laboratory Technician.
- Higher job levels, like Director and Manager, have low percentage of attrition.
- Manufacturing Directors have highest  Environment Satisfaction, while Healthcare Representative have highest Job Satisfaction, and Human Resources have highest Work Life Balance.

[Back to Top](#BackToTop)


---
<a name="P3"></a>

## Employee Attrition Classification Model Using KNN
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/KNN_Summary.png?raw=true" style="left" width="400"/>

Wiht K = 21, the model achieved the **accuracy of 86.7%** with the 95% CI of Accuracy of (83.7%, 89.3%).

[Back to Top](#BackToTop)

---
<a name="P4"></a>

## Employee's Monthly Income Prediction Using MLR
<img src="https://github.com/Purifect/Employee_Attrition_Prediction/blob/main/photos/KNN_Summary.png?raw=true" style="left" width="400"/>

Wiht K = 21, the model achieved the **accuracy of 86.7%** with the 95% CI of Accuracy of (83.7%, 89.3%).

[Back to Top](#BackToTop)

---
