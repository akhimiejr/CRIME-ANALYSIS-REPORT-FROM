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

