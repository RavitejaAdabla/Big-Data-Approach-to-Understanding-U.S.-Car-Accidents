# Big Data Analysis of U.S. Car Accidents
An end-to-end big data project to analyze and predict the severity of car accidents across the United States. This analysis leverages a large-scale dataset (2016-2021) to identify key factors contributing to accidents and builds a machine learning model to forecast their severity.

## Project Goal
The primary objective is to analyze traffic accident data to uncover patterns related to time, location, and environmental factors. The ultimate goal is to build a predictive model that can accurately forecast accident severity, providing actionable insights for traffic safety authorities to implement preventative measures.

**Key Objectives:**  
**Analyze Trends:** Investigate accident occurrences across states, cities, months, and time of day.  
**Feature Engineering:** Engineer meaningful features from raw data to improve model performance.  
**Predict Severity:** Develop and evaluate multiple machine learning models to predict accident severity (ranging from 1-4).  
**Provide Recommendations:** Offer data-driven insights that can help authorities reduce accident frequency and severity.  

## Methodology & Tech Stack
This project utilizes big data tools and a standard machine learning workflow to process and model the data.

**Core Technologies:** Python, Pandas, Apache Spark (for handling large datasets).  
**Machine Learning:** Scikit-learn.  
**Models Used:** Logistic Regression, Decision Tree, Random Forest.  

**Data Processing & Feature Engineering:**  
**Data Ingestion:** Loaded the U.S. Car Accidents dataset covering 2016-2021.  
**Feature Transformation:**  
Converted raw start_time and end_time columns into more predictive features like hour_of_day and day_of_week.  
Utilized One-Hot Encoding to transform categorical variables into a numerical format suitable for machine learning algorithms.  
**Handling Class Imbalance:**  
The Severity variable was highly imbalanced, with a prevalence of "Severity 2" accidents.  
To create a more stable model, "Severity 1" and "Severity 2" were consolidated into a single "Low Severity" category for binary classification tasks, effectively balancing the dataset.  
**Data Splitting:** The dataset was partitioned into a 70% training set and a 30% validation set.  

## Key Analytical Insights
The exploratory data analysis revealed several distinct patterns in U.S. car accidents:

**Geographic Hotspots:**  
**State Level:** California has the highest number of reported accidents nationwide.  
**City Level:** Miami reports the highest number of accidents.  
**Temporal Trends:**  
**Monthly:** December sees the highest frequency of accidents.  
**Yearly:** 2021 recorded the most accidents in the dataset.  
**Weekly:** Accidents peak on Fridays and decrease significantly over the weekend.  
**Severity Distribution:**  
"Severity 2" is the most common type of accident.  
Severe accidents (Severity 4) do not appear to be concentrated at any specific time of day.  

## Model Performance
The Random Forest model demonstrated superior performance in predicting accident severity compared to other algorithms. This model's high accuracy and AUC score, especially on the balanced dataset, make it the most reliable model for this prediction task. Feature importance plots from the model identified Year, Wind Speed, and Hour as the most significant predictors.

## Actionable Recommendations for Authorities
**The insights from this analysis can be used to develop targeted safety interventions:**

**Strategic Resource Allocation:** Law enforcement and safety patrols should be increased in high-risk areas like California and Miami, especially during peak accident times.  
**Targeted Enforcement:** With Fridays and the month of December identified as high-frequency periods, authorities can plan targeted campaigns to enforce traffic laws and raise driver awareness during these times.  
**Daytime Safety Measures:** Since accident severity appears to increase during daytime hours, public awareness campaigns should emphasize the need for heightened caution while driving during the day.  
This project successfully demonstrates how big data analysis can provide critical insights into traffic safety, offering a clear path for authorities to make data-informed decisions that can potentially save lives.


