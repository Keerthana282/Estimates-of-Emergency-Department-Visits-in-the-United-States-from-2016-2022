# Estimates-of-Emergency-Department-Visits-in-the-United-States-from-2016-2022
Project Overview & Objective
This project focuses on analyzing national-level Emergency Department visit
estimates between 2016 and 2022. The dataset includes yearly estimates along with
confidence intervals, demographic groupings, and visit classifications.
To analyze and visualize Emergency Department (ED) visit estimates in the United
States from 2016 to 2022 in order to identify trends, demographic patterns, and
changes over time.
#Data Sources
● Source Description and Timeline: Data government
● Domain: Health Care

## 🎯Problem Statement
• Evaluate year-over-year growth and decline in ED visits
• Identify variations across age groups, gender, and visit categories
• Examine trends before, during, and after the COVID-19 period
• Transform raw healthcare data into meaningful insights using Excel and
Power BI
• Build an interactive dashboard to support data-driven healthcare
decision-making

##🧰 Tools & Technologies
• Excel: Data cleaning , Power Query
• Power BI: Data modelling, DAX calculations, visualization, and
interactive dashboard creation.

#⌛Data Cleaning & Transformation
• Cleaned the Emergency Department (ED) visit dataset by checking for
inconsistencies and missing values.
• Standardized column formats (Year converted to numeric format, Estimate
and statistical fields converted to decimal).
• Renamed columns for clarity and consistency.
• Validated numerical fields such as Estimate, Standard Error, Lower 95% CI,
and Upper 95% CI.
• Ensured categorical columns (Measure Type, Group, Subgroup, Estimate
Type) were properly formatted for modeling.
Conversion into Fact and Dimension Tables
The dataset was transformed from a flat structure into a Star Schema model to
improve performance and analytical flexibility.

#🗃️DAX FORMULAS

AverageVisit =
AVERAGEX(Dim_Estimate,Dim_Estimate[Estimate])

AvgCurrentYearVisit = Calculate([Averagevisit],
factTable[year]=2022)

AvgPreviousYearVisit = Calculate([Averagevisit],
factTable[year]=2021)

YoY = Divide ([AvgCurrentYearVisit ] –
[AvgPreviousYearVisit] , [AvgPreviousYearVisit])

#🎯DASHBOARD AND INSIGHTS:

From 2016 to 2019, emergency visits were generally stable to increasing.
In 2020, something changed visits dropped.
After that, things started recovering but never fully returned to pre-2020 peaks.

<img width="779" height="515" alt="Emergency_Visit _Avg" src="https://github.com/user-attachments/assets/28682633-99e7-4db5-b58d-c85a1a599c4b" />


Average Estimates

# 📌Overall ED Visits Trend (2016–2022)
• Visits were relatively strong from 2016 to 2019
• Peak around 2019
• Sharp drop in 2020
• Partial recovery in 2021
• Drop again in 2022
• YoY change: -15.39%
• Visits dropped from 7.62M (previous year) to 6.45M (this year)

##📊The pattern is:
Stable growth → Pandemic shock → Recovery → Decline again

<img width="459" height="341" alt="Insurance survey" src="https://github.com/user-attachments/assets/80d2550e-8afc-42b5-8715-7a0cc0ef2251" />

• Medicaid & Medicare hold large volume consistently
• Private insurance fluctuates
• Uninsured gradually increases toward 2022

<img width="387" height="230" alt="Avg gender visit" src="https://github.com/user-attachments/assets/ec94148e-67ae-452d-9c74-bf2df45e242f" />

## 🔵Gender Distribution

<img width="387" height="212" alt="Gender" src="https://github.com/user-attachments/assets/610e2bee-cdf5-417b-bad2-1f42e0685c3a" />

• Female visits slightly higher ~28–29%
• Male slightly lower 24–26%

## 📈 Age Distribution
• 18–44 years = Highest visits ~34%
• Followed by 45–64
• 0–17 and 65+ lower comparatively
Working-age adults dominate ED visits.

##📊 Regional Standard Error

• Highest uncertainty around 2019–2020
• 2020 shows highest variability
• Lower again by 2022
Pandemic period = unstable data pattern.

 ##☑️Over all Dashboard

 
<img width="709" height="513" alt="Analysis on Emergency visit in US_(Dashboard)" src="https://github.com/user-attachments/assets/139421c7-59c1-4374-a4cf-bdf03c75c27f" />


##📍 Conclusion:
This dashboard tells me a story of shock and adaptation.2019 was the peak.2020
disrupted everything. The system never fully returned to its previous trajectory.
The decline in visits isn’t random it reflects behavioral change, telehealth
adoption, and possibly improved care routing.
