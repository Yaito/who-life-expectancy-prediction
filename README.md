# Life expectancy prediction

## Overview

The goal of this project is to do an analysis of public health data from the World Health Organization (WHO) to answer key questions regarding global life expectancy trends and the construction of a model capable of predicting life expectancy based on country, social, economic characteristics, vaccines coverage, and many others features.

## Use Case Understanding

Although there have been lot of studies undertaken in the past on factors affecting life expectancy considering demographic variables, income composition and mortality rates. It was found that affect of immunization and human development index was not taken into account in the past. Also, some of the past research was done considering multiple linear regression based on data set of one year for all the countries. Hence, this gives motivation to resolve both the factors stated previously by formulating a regression model based on mixed effects model and multiple linear regression while considering data from a period of 2000 to 2015 for all the countries. Important immunization like Hepatitis B, Polio and Diphtheria will also be considered.

<img src="images/life expectancy through the years.png" width="500">

## Data Understanding

The Global Health Observatory (GHO) data repository under World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries. The dataset related to life expectancy, health factors for 193 countries has been collected from the same WHO data repository website and its corresponding economic data was collected from United Nation website. Among all categories of health-related factors only those critical factors were chosen which are more representative. Therefore, in this project we have considered data from year 2000-2015 for 193 countries for further analysis. The individual data files have been merged together into a single dataset. On initial visual inspection of the data showed some missing values. As the datasets were from WHO, we found no evident errors. The final dataset consists of 22 Columns and 2938 rows which meant 20 predicting variables. All predicting variables was then divided into several broad categories:​Immunization related factors, Mortality factors, Economical factors and Social factors.

<img src="images/life expectancy distribution.png" width="500">

## Model and Evaluation

This project aimed to predict life expectancy using various socio-economic and health-related factors. Initial modeling with a Random Forest regressor achieved excellent performance (R² ≈ 0.97, MSE ≈ 2.13), but relied heavily on country-specific information, hindering generalization.

Subsequent feature engineering and selection, including combining immunization metrics and removing multicollinear features, created a more generalized model. While the R² slightly decreased (to ≈ 0.95) and MSE increased (to ≈ 3.75), this new model provides more actionable insights by focusing on factors like HIV/AIDS prevalence, adult mortality, schooling, infant mortality, and childhood malnutrition.

<img src="images/features importance.png" width="500">

## Conclusion

By including new factors such as immunization and human development index to the analysis, the model demonstrated that simply increasing healthcare expenditure might not directly translate to higher life expectancy, highlighting the need for efficient resource allocation.

Based on the model's findings, several key areas warrant focus for improving global life expectancy:
- Combatting HIV/AIDS: The model identifies HIV/AIDS as the most significant factor impacting life expectancy. Increased investment in prevention, treatment, and awareness programs is crucial.List
- Improving Education and Nutrition: The significant influence of schooling and malnutrition indicators suggests that addressing these issues seems to be key factors. Investments in education infrastructure, teacher training, and accessible nutritional programs can yield substantial improvements in life expectancy.
- Reducing Infant and Adult Mortality: High rates of infant and adult mortality negatively correlate with life expectancy. Focus should be placed on maternal and child healthcare, as well as addressing underlying causes of adult mortality.
- Efficient Healthcare Resource Allocation: The model suggests that simply increasing healthcare spending is not a guarantee of improved life expectancy. Governments and organizations should prioritize strategic resource allocation, targeting specific areas based on the identified factors influencing life expectancy. Further research on the effective use of healthcare spending can inform policy decisions.
