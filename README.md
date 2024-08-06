# Big-Data-Approach-to-Understanding-U.S.-Car-Accidents
# Premise
Over the years, the demand for transportation has shifted from public to private modes, with most people in the United States now relying on private transportation. This increasing demand, coupled with developments in transportation infrastructure, has brought about significant traffic safety challenges. Car accidents are prevalent worldwide, and the cost of vehicle crashes and driver injuries has a substantial impact on society.

In this analysis, we aim to examine the number of accidents occurring across different states and cities, throughout the year, and during various months. Our goal is to estimate the severity of these accidents and gain insights into traffic safety trends.

# Goal
The goal of this project is to conduct an analysis to predict the severity of car accidents across the United States using big data tools. This study will investigate the occurrence of accidents in various states and cities, considering data from 2016 to 2021. Additionally, it will analyze the timing of these accidents throughout different times of the day to provide comprehensive insights.

# Feature Engineering and Data Modelling
A crucial step in developing any machine learning model is feature engineering. Since many algorithms perform better with numerical data, we utilized One-Hot Encoding to convert categorical attributes into numerical format using dummy variables.

Our analysis did not gain significant insights from time-related variables indicating when the accident started and ended. Instead, we transformed these features into more relevant ones, such as the day of the week and the hour of the day.

The primary variable, Severity, ranges from 1 to 4. The dataset is imbalanced, with a high frequency of Severity 2 observations compared to the rarer Severity 1 instances. To address this imbalance, we consolidated Severity 1 and 2 into a single category, Severity 2.

We split the dataset into training and validation sets, with 70% of the data used for training the models and the remaining 30% reserved for validation. This approach allows for both multiclass and binary classification using the processed data.

Machine Learning Algorithms that are used include Logistic regression, Decision tree, and Random Forest.

# Results
## State Analysis: 
California reports the highest number of accidents among all U.S. states.
## City Analysis: 
Within California, Miami has the highest number of accidents.
## Monthly Analysis: 
Severity 2 accidents are the most common across months, with December recording the highest number of accidents. The year 2021 experienced the most accidents overall.
## Severity Distribution: 
Severity 2 has the highest frequency of accidents, while Severity 3 and 4 are the least common.
## Time of Day: 
Severe accidents (Severity=4) occur throughout the day, with no specific time showing a higher frequency.
## Day of the Week: 
Friday has the highest number of accidents from 2016 to 2021. The accident rate significantly decreases over the weekends.
## Model Performance: 
The Random Forest model outperforms other models in predicting accident severity, achieving an accuracy of 81.67% and an AUC ROC of 84.26%.

# Conclusion
Our exploratory data analysis revealed that certain factors, such as the day of the week, hour of the day, and month of the year, exhibit significantly high accident frequencies. Authorities can use this information to strategically plan and enforce stricter traffic laws during these peak times to potentially reduce accident numbers.

We observed that accident severity tends to increase during the day, indicating a need for heightened safety measures and precautions during daytime hours.

Feature importance plots identified Year, Wind Speed, and Hour as significant predictors in forecasting accident severity. Among the models tested, the Random Forest model performed best in terms of accuracy and AUC ROC score, particularly when applied to a balanced dataset.
