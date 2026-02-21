# health-tech-engagement-data-study
An end-to-end data analysis project using **Spreadsheets, SQL, Python, and Tableau** to identify growth opportunities in user activity trends for a health-tech company

# From Sedentary to Active: Identifying Growth Opportunities in the Bellabeat Ecosystem

## 📊 Project Overview
This project analyzes smart device fitness data to provide strategic marketing recommendations for **Bellabeat**, a high-tech manufacturer of health-focused products for women. Using the Google Data Analytics framework **(Ask, Prepare, Process, Analyze, Share, Act)**, I identified key correlations between activity intensity and caloric expenditure to drive user engagement.


# 🧬 Case Study: Identifying Growth Opportunities in Health-Tech
**Author:** Prosper Wiredu Ackah  
**Tools:** SQL (BigQuery), Python (Pandas/Seaborn), Tableau, Spreadsheets  
**Data Source:** FitBit Fitness Tracker Data (CC0 Public Domain)

---

## 1. Ask: The Business Challenge
The objective is to analyze how consumers use non-Bellabeat smart devices to provide high-level recommendations for Bellabeat’s marketing strategy. 

**Core Questions:**
1. What are the trends in smart device usage?
2. How do these trends apply to Bellabeat customers?
3. How can these trends influence Bellabeat marketing strategy?

---

## 2. Prepare: Data Sources & Scope
The analysis utilizes the FitBit Fitness Tracker Data (30 days of activity data). 
* **Population ($N$):** 35 unique users.
* **Granularity ($n$):** 457 daily observations across the study period.
* **Storage:** Data was processed using BigQuery for aggregation and structured in Python for statistical validation.

---

## 3. Process: Data Integrity & Scientific Pivot
To maintain professional rigor, a comprehensive data audit was conducted prior to analysis.

* **The Audit:** A significant **temporal mismatch** was identified between the activity logs (March–April) and the sleep/weight logs (April–May).
* **The "Scientific Pivot":** To avoid "low-power" conclusions based on limited overlapping data, the analysis was pivoted to focus on the correlation between **Activity Intensity and Metabolic Outcomes** within the comprehensive set of 457 daily observations. This ensured the analysis was grounded in a statistically significant sample.
* **Cleaning Procedures:** * Removed null values and duplicates in the daily activity set.
    * Converted "ActivityDate" strings into uniform `Date` objects.
    * Standardized column naming conventions for seamless SQL joining.

---

## 4. Analyze: Technical Logic & Statistical Validation

### A. Feature Engineering (SQL)
Used **SQL Window Functions** to engineer a 3-tier User Activity Index based on 31-day rolling averages:
* **Sedentary:** < 5,000 avg steps (~40% of the sample).
* **Fairly Active:** 5,000–10,000 avg steps.
* **Active:** > 10,000 avg steps.

### B. Statistical Rigor (Python)
Utilized Python to mathematically validate visual trends found in the dashboard. A **Pearson Correlation Coefficient ($r$)** was calculated between "Very Active Minutes" and calories burned.
* **Result:** **$r = 0.64$**
* **Conclusion:** There is a strong positive correlation, proving that high-intensity effort is a more efficient metabolic driver than pure step volume.

---

## 5. Share: Key Behavioral Insights

* **The "Saturday Peak" vs. "Mid-Week Slump":** Analysis reveals a significant activity surge on Saturdays for the **Active** group, while a recurring engagement dip occurs on **Tuesdays and Thursdays** across all segments.
* **The Efficiency Gap:** Data proving that "Very Active Minutes" are the most efficient way for users to burn calories compared to pure step volume.

---

## 6. Act: Strategic Recommendations

1. **Prioritize Intensity over Volume:** Shift marketing focus from "10,000 steps" to "20 Minutes of High-Intensity Activity" to align with metabolic efficiency.
2. **Weekend Engagement:** Capitalize on the existing "Saturday Peak" with specific community challenges and rewards.
3. **Mid-Week Recovery Triggers:** Implement notifications on Tuesdays/Thursdays to combat the identified engagement slump across all user types.
4. **Target the Sedentary 40%:** Develop a specific "Onboarding Journey" for sedentary users that focuses on slowly increasing "Fairly Active Minutes" to build long-term habits.

## 📈 Key Insights
* **High-Intensity Impact:** A strong positive correlation confirms that "Very Active Minutes" are the primary driver of calorie burn.
* **The "Saturday Peak":** Highly active users show a **25%** surge in weekend activity, while sedentary users remain **flat**.
* **Growth Target:** **40%** of the sample is currently sedentary, representing a massive market for entry-level engagement features.

## 6. Act: Strategic Recommendations

Based on the evidence above, I recommend the following four-pillar strategy to enhance Bellabeat’s market position and user health outcomes:

### A. Prioritize "Intensity" Over "Volume"
* **The Strategy:** Shift marketing narratives from the "10,000 Step Goal" to **"The 20-Minute Daily Intensity Target."**
* **Why:** Our $r=0.64$ correlation proves that high-intensity effort is a more efficient metabolic driver. This makes health goals more achievable for busy users while delivering better results.

### B. Capture the "Sedentary 40%" (Market Growth)
* **The Strategy:** Develop a **"Beginner’s Onboarding Journey"** specifically for the sedentary segment.
* **Why:** This 40% represents the biggest growth opportunity. By focusing on "Fairly Active Minutes" rather than "Active" status, Bellabeat can build long-term habits and increase app subscription retention for new users.

### C. Combat the "Mid-Week Slump"
* **The Strategy:** Implement **Mid-Week "Power Triggers"** via the Bellabeat app on Tuesdays and Thursdays.
* **Why:** Data shows a consistent dip in engagement during these days. Targeted push notifications or "Mini-Challenges" can help maintain user momentum throughout the work week.

### D. Capitalize on the "Saturday Peak"
* **The Strategy:** Launch **"Saturday Community Challenges"** with rewards for group participation.
* **Why:** Since the data shows a natural 25% surge in activity on Saturdays, Bellabeat should lean into this existing behavior to foster a sense of community and social competition among users.



---

## 7. Limitations & Caveats
To maintain scientific integrity, the following constraints of the FitBit dataset and this analysis must be acknowledged:

* **Demographic Specificity:** While Bellabeat’s target audience is women, the public FitBit dataset does not explicitly identify the gender or age of the 35 participants. This creates an External Validity risk; the physiological baseline of this cohort may not perfectly represent the specific metabolic profiles of Bellabeat’s primary users.
  
* **Nutritional Confounders:** Metabolic output is heavily influenced by caloric and macronutrient intake. This dataset lacks nutritional data, meaning the analysis cannot account for the "Thermic Effect of Food" or metabolic variations caused by pre-exercise fueling.
  
* **Sample Size (N=35):** While **457** observations (n) provide sufficient power for correlation analysis, the limited number of unique individuals increases the risk of **Sampling Bias**. The habits of a few highly active outliers may disproportionately influence the overall trends.

*  **Study Duration:** This analysis represents a 31-day snapshot. It does not account for long-term behavioral changes, seasonal activity variations, or the longitudinal habit-formation cycles essential for a wellness coaching strategy.

---
 |
[Tableau Dashboard](PASTE_YOUR_TABLEAU_URL_HERE)
[LinkedIn](https://www.linkedin.com/in/p-ackah)








## 📊 Data Scope
To ensure high statistical power and granular insights, this analysis distinguishes between the study population and individual observations: 

* **Unique Users (N=35):** Unique Users **(N=35)**: Represents the distinct individuals in the cohort, used for market segmentation and determining high-level audience      composition.
* **Total Observations (n=457):** Represents the total number of daily activity records analyzed across the study period.
  
By utilizing the full dataset of **457** observations for correlation analysis **(r=0.64)**, this project achieves a higher level of mathematical rigor than would be possible using user-level averages alone.

## 🛠️ Technical Stack
* **SQL (BigQuery):** Data cleaning and User Segmentation via Window Functions.
* **Python (Pandas/Seaborn):** Statistical validation and Pearson Correlation **(r = 0.64)**.
* **Tableau:** Interactive dashboarding and executive-level storytelling.

## 🧪 The Scientific Challenge (Data Integrity Audit)
Coming from a **Research Science background**, I prioritized data auditing. I discovered a significant date-mismatch between the activity and sleep datasets. To maintain statistical power and data integrity, I pivoted the analysis to focus on **Activity Intensity vs. Metabolic Outcomes**, ensuring a robust sample size of **457** observations.

## 📈 Key Insights
* **High-Intensity Impact:** A strong positive correlation confirms that "Very Active Minutes" are the primary driver of calorie burn.
* **The "Saturday Peak":** Highly active users show a **25%** surge in weekend activity, while sedentary users remain **flat**.
* **Growth Target:** **40%** of the sample is currently sedentary, representing a massive market for entry-level engagement features.




## 🔗 Live Dashboard
https://public.tableau.com/app/profile/prosper.ackah/viz/HealthcareDataAnalysisProject_17714843701280/FromSedentarytoActive?publish=yes


