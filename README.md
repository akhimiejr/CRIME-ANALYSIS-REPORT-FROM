## 1	Part 1 – Understand the Data Set and Descriptive Visualization
# 1.1	Introduction
A Data-Driven Journey into the Heart of Crime in Los Angeles" explores the city's complex crime patterns, with a focus on the disproportionate impact on marginalized communities. The project analyzes various crime types, such as vio-lent and non-violent crimes, to understand their frequency, affected de-mographics, times of occurrence, and geographical distribution. Using Python, Jupyter Notebook, and libraries like pandas, matplotlib, seaborn, scikit-learn, and plotly, the analysis employs machine learning models (Logistic Regression, Deci-sion Trees, and Random Forest) to predict crime likelihood and identify key fac-tors. The practical applications are significant, enabling financial institutions to prevent crime and the LAPD to optimize patrols based on crime patterns. The study also integrates current crime detection and prevention methodologies, such as statistical analysis, GIS for spatial insights, and real-time alert systems, aiming to enhance public safety and resource allocation in Los Angeles.
# 1.2	Dataset Description
This dataset contains detailed records of 944,000 crime incidents reported to the Los Angeles Police Department (LAPD), each row representing a unique inci-dent with 28 attributes. Key columns include identifiers like DR_NO, dates and times of occurrence and reporting, geographic details such as area codes and names, descriptions and codes for the crimes committed, victim demographics, premises types, weapon details, case statuses, and location coordinates. The data is designed for analyzing crime trends, geographic patterns, and victim characteris-tics, and can be accessed through the LA City GeoHub. This dataset display crime rate from Los Angeles from 2020 to date. The information is digitized from origi-nally documented crime reports, which may introduce some inaccuracies. Location fields with missing data are recorded as (0°, 0°)
# Summary Statistics of The Dataset
. Descriptive statistics offer a summary of the central tendency, variability, and distribution shape of the dataset after it was uploaded into my Python software.

![image](https://github.com/user-attachments/assets/ae6faac9-48bb-44e7-b2b5-d5739723347e)

# Plot-Based Data Visualization
. Pie-Chart of Gender Distribution of Crime Victims

![image](https://github.com/user-attachments/assets/e794f158-eeb0-4706-8f21-35417ca70c5d)

The above visual shows a distribution of crime victims by gender where F- female, M- male, while H and X is Unknown
# Crime Rate in Different Region or District

![Screenshot 2024-05-23 111746](https://github.com/user-attachments/assets/020e8bc9-b0a9-4692-a370-241e9fbfb97b)

The above visual shows the different rate of crime in different rejoin where Central prove to be the highest affected area.
# Pie Chart Showing Top Weapons Used in Crimes

![Screenshot 2024-05-23 113006](https://github.com/user-attachments/assets/8098c93d-fb23-483e-9d02-f3b5793be330)

The visual above generates a pie chart to visualize the distribution of weapons used in crimes, highlighting the top 10 most frequently used weapons. 

## Part 2 – Explore Relationships in the Data Set
# 2.1	Exploring Relationships in the Dataset
Correlation Analysis:
![Screenshot 2024-05-23 123602 (1)](https://github.com/user-attachments/assets/48532545-8809-401a-ac67-7a04c4ac2cfa)

Correlation analysis helps identify the strength and direction of relationships between variables. This is crucial for understanding how different factors such as time, location, and demographics influence crime rates.

# Scatter Plots and Pair Plots

![Screenshot 2024-05-23 124406](https://github.com/user-attachments/assets/c510b9da-2521-49c0-af94-3cec5855ed1b)

The interactive map helps users analyze the geographic distribution of different types of crimes, providing insights into where and when crimes occur.

# Time Series Analysis

![Screenshot 2024-05-23 134108](https://github.com/user-attachments/assets/c160c447-4670-4af9-9efc-9fb182c908a1)

The graph titled "Trend of Crime per Hour" shows the number of crimes occur-ring each hour over a 24-hour period, highlighting a significant peak at noon (~60k crimes) and a low around 5 AM (~10k crimes). Crime rates gradually decrease from midnight to early morning, spike sharply at noon, then decline and stabilize with minor fluctuations in the afternoon before decreasing again in the evening. These trends suggest the need for increased law enforcement and public awareness dur-ing high-crime periods, especially around noon, while potentially reallocating re-sources during low-crime early morning hours to optimize safety and security ef-forts.

## 3	Part 3 – Independent Evaluation and Commentary
# 3.1	Machine Learning: Service Details and Model Selection
Service Details: The machine learning service developed in this project aims to predict the likelihood of crimes occurring based on various factors such as time, location, and demographic information. This predictive service can be utilized by law enforcement agencies to enhance proactive crime prevention strategies and optimize resource allocation. By analyzing patterns in historical crime data, the service can identify high-risk periods and locations, enabling law enforcement to deploy resources more efficiently and potentially reduce crime rates.
Model Selection: Different machine learning models were considered for this pro-ject, each with distinct strengths and suitability for the task:
# Logistic Regression:
Suitability: Logistic Regression especially apt as to binary classification tasks, in which the objective is aimed at predicting at least a possible outcomes (e.g., whether a crime will happen or not in each situation).
Strengths: This model delivers interpretable outcomes through coefficients that signify the connection between features and the probability of crime occurrence. It is computationally efficient and adept at handling large datasets.
Limitations: Logistic Regression assumes a linear connection between the features and the log-odds of outcomes, which may not sufficiently capture more complex patterns in the data.
  
# Decision Trees:
Suitability: Decision Trees are applicable to both classification and regression tasks, especially excelling when the connections between features and outcomes are non-linear.
Strengths: They are straightforward to visualize and interpret, offering clear insights into the decision-making process. Each node in the tree represents a feature and a threshold, making it easy to comprehend how predictions are determined.
Limitations: Decision Trees can be prone to over-fitting, especially with complex datasets Over-fitting happens when the model learns the noise in the training data instead of the actual patterns, resulting in poor performance on new, unseen data.

![Screenshot 2024-05-23 162807](https://github.com/user-attachments/assets/92252134-07b0-4164-a4f9-bd3bf7497082)

# Random Forests:
Suitability: Random Forests, an ensemble learning method, are well-suited for tasks requiring high accuracy and robustness. They aggregate the predictions from multiple decision trees to enhance overall performance
Strengths: This model offers better accuracy and robustness compared to individ-ual decision trees by averaging the results of multiple trees, which reduces the risk of over-fitting. Random Forests also handles large datasets and high-dimensional data well.
Limitations: While Random Forests improve accuracy and generalization, they can be less interpret-able than single decision trees. Understanding the contribution of individual features requires additional techniques, such as feature importance analysis.

![Screenshot 2024-05-23 215157](https://github.com/user-attachments/assets/d33cd536-9721-46f5-a6d3-5acedb2fef04)

# Model Selection for Crime Prediction:
In this project, the Random Forest model was more preferred for its superior per-formance in terms of accuracy and robustness. As illustrated in the feature im-portance analysis, the Random Forest model effectively identified 'Weapon Used Cd Log' as the most significant predictor, followed by 'Time of Occurrence' and 'Victim Age'. This insight underscores the model’s capability to discern complex patterns and interactions among features, which is crucial for accurate crime pre-diction. By deploying the Random Forest model, the service leverages the strengths of ensemble learning to provide reliable predictions that law enforce-ment agencies can trust for strategic decision-making. The focus on key predictive features enables targeted interventions, ultimately contributing to more effective crime prevention and resource management 

# 3.2	 Evaluation
Correctness: The ratio of accurately forecast instances among the entire cases. Precision: The ratio of accurately identified positive forecasts among all positive forecasts generated by the model. Completeness: The ratio of accurately identi-fied positive forecasts among all real positive instances. F1-measure: The harmon-ic average of Precision and Completeness, considering both incorrect positive and negative predictions

![image](https://github.com/user-attachments/assets/b89ad763-77d8-4d00-ac23-9facba05b8b2)

# 3.3	Conclusion 
This project successfully analyzed crime data in Los Angeles, providing insights into the types, frequency, and patterns of crimes. Machine learning models were developed to predict the likelihood of crimes, offering a tool for proactive crime prevention.The findings of this project have practical implications for law en-forcement agencies in Los Angeles. By understanding crime patterns and predict-ing potential incidents, agencies can allocate resources more efficiently and im-plement targeted interventions to reduce crime rates and enhance public safety.

## APPENDIX

![image](https://github.com/user-attachments/assets/ee5eea57-be81-411b-b051-10d7c12ddd32)

Appendix 1.

![image](https://github.com/user-attachments/assets/f708529f-4379-4a5b-96f9-c75c8d1a6bc7)

Appendix 2. 

![image](https://github.com/user-attachments/assets/c9015a77-f5e9-4531-a1cf-77e6ea79ad3c)

Appendix 3.

![image](https://github.com/user-attachments/assets/38bf681a-8a83-426e-add7-7e5947bf2a23)

Appendix 4.

![image](https://github.com/user-attachments/assets/09a69133-a2ae-40f5-a11d-f78e5fcfe9db)

Appendix 5. 

![image](https://github.com/user-attachments/assets/4cfb62e9-ddc7-49c2-9913-285ab3a780fd)

Appendix 6.

![image](https://github.com/user-attachments/assets/ccd55ae2-2318-4495-8ac3-90cd54e12120)

Appendix 7. 

![image](https://github.com/user-attachments/assets/3f77a70b-11d9-475c-b497-1af41f6c4422)


Appendix 8.














