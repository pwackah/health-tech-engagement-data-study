# health-tech-engagement-data-study
An end-to-end data analysis project using Spreadsheets, SQL, Python, and Tableau to identify growth opportunities in user activity trends for a health-tech company

# From Sedentary to Active: Identifying Growth Opportunities in the Bellabeat Ecosystem

## 📊 Project Overview
This project analyzes smart device fitness data to provide strategic marketing recommendations for **Bellabeat**, a high-tech manufacturer of health-focused products for women. Using the Google Data Analytics framework (Ask, Prepare, Process, Analyze, Share, Act), I identified key correlations between activity intensity and caloric expenditure to drive user engagement.

## 📊 Data Scope
To ensure high statistical power and granular insights, this analysis distinguishes between the study population and individual observations: 

  a. Unique Users (N=35): Represents the distinct individuals in the cohort, used for market segmentation and determining high-level audience composition.
  b. Total Observations (n=457): Represents the total number of daily activity records analyzed across the study period.
  
By utilizing the full dataset of 457 observations for correlation analysis (r=0.64), this project achieves a higher level of mathematical rigor than would be possible using user-level averages alone.

## 🛠️ Technical Stack
* **SQL (BigQuery):** Data cleaning and User Segmentation via Window Functions.
* **Python (Pandas/Seaborn):** Statistical validation and Pearson Correlation (r = 0.64).
* **Tableau:** Interactive dashboarding and executive-level storytelling.

## 🧪 The Scientific Challenge (Data Integrity Audit)
Coming from a **Research Science background**, I prioritized data auditing. I discovered a significant date-mismatch between the activity and sleep datasets. To maintain statistical power and data integrity, I pivoted the analysis to focus on **Activity Intensity vs. Metabolic Outcomes**, ensuring a robust sample size of 457 observations.

## 📈 Key Insights
* **High-Intensity Impact:** A strong positive correlation confirms that "Very Active Minutes" are the primary driver of calorie burn.
* **The "Saturday Peak":** Highly active users show a 25% surge in weekend activity, while sedentary users remain flat.
* **Growth Target:** 40% of the sample is currently sedentary, representing a massive market for entry-level engagement features.

## 🔗 Live Dashboard
https://public.tableau.com/app/profile/prosper.ackah/viz/HealthcareDataAnalysisProject_17714843701280/FromSedentarytoActive?publish=yes
