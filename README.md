What Drives Emergency Department Wait Times Across U.S. Hospitals?
A data analytics project examining why emergency department (ED) wait times differ across U.S. hospitals and how those delays affect patients.

Course: BA780, Boston University Questrom School of Business
Project: A04 Final Project, Cohort A, Team 4
Tools: Python, pandas, NumPy, Matplotlib, Plotly, Jupyter Notebook, and machine learning libraries
Project Overview
Emergency department wait times vary significantly across the United States. This project analyzes 4,080 hospitals to explore the relationship between ED wait times, hospital volume, patient flow, hospital characteristics, and state economic conditions.

Using public data from the Centers for Medicare & Medicaid Services (CMS) and the U.S. Census Bureau, our team combined three datasets, cleaned and merged the records, created visualizations, and used correlation analysis and linear regression to identify patterns that could inform hospital operations decisions.

Main measure: OP_18b, the median time spent in the ED from arrival to departure, excluding psychiatric and transfer patients.
Key Questions
1. Are busier emergency departments associated with longer wait times?
2. How do wait times relate to patients leaving before receiving care?
3. Which patient groups experience the longest stays?
4. How do hospital ownership, quality ratings, and rural status relate to wait times?
5. Do state economic conditions help explain differences in ED performance?
Key Findings
ED volume and wait time: Median ED visits increase from 120 minutes in low volume EDs to 192.5 minutes in very high volume EDs.

Patients leaving without being seen: The average share rises from 0.70% at hospitals with median visits under two hours to 3.91% at hospitals over four hours. This is approximately 5.6 times higher.

Correlation with patients leaving: Median ED time and the percentage of patients leaving before being seen have a positive correlation of 0.52.

Psychiatric and transfer patients: Among very high volume EDs, the slowest quarter reports median psychiatric stays of 368 minutes, compared with approximately 222 minutes in the fastest quarter.

Hospital ratings: Overall hospital star ratings explain less than 1% of the observed variation in ED wait times in the notebook's comparison.

State comparison: Massachusetts has a median ED time of 211.5 minutes, compared with 126 minutes in Minnesota. Differences in ED size and rural hospital mix help explain this gap.

These results describe observational associations, not proof that any individual factor causes longer waits.
My Contribution: Patient Experience Analysis
I worked on the project's patient experience analysis (Part 2, Charts 9 and 10). My work examined how longer ED stays relate to patients leaving before being seen, along with psychiatric and transfer patient wait times across hospital volume groups and states.

My analysis included the following:
1. Grouping hospitals by median ED duration and comparing the percentages of patients who left before receiving care.
2. Examining the relationship between ED duration and patients leaving without being seen.
3. Comparing psychiatric and transfer patient stays across ED volume categories.
4. Exploring differences in psychiatric wait time gaps among states.
5. Estimating potential improvements in patient retention under benchmark scenarios.
Patient impact: The analysis estimated that approximately 116,338 additional patients per year could remain to be seen if 142 very high volume EDs with median visits exceeding four hours reduced their rates of patients leaving to those observed in the group with median visits between three and four hours. This is a scenario estimate, not a validated forecast.
Data Sources
1. CMS Timely and Effective Care, Hospital: ED wait time metrics, ED volume, and patients leaving without being seen.
2. CMS Hospital General Information: Hospital characteristics, ownership, and overall star ratings.
3. U.S. Census Bureau, 2024 ACS One Year, Table DP03: State income, employment, insurance, and commuting statistics.
The notebook retrieves three CSV files from the team data repository.
Methods and Tools
Data preparation: Reshaped CMS measures, converted missing value strings into NaN, preserved hospital IDs as text, and merged hospital and Census data.

Exploratory data analysis: Summarized and compared results by hospital size, ownership, patient category, and state.

Visualization: Created histograms, bar charts, scatter plots, and U.S. choropleth maps.

Statistical analysis: Used correlations, comparisons within hospital groups, and state level linear regression.
How to Run the Project
1. Download or clone this repository.
2. Open [`FInal A04 What Drives ER Wait Times.ipynb`](FInal%20A04%2DWhat%2DDrives%2DER%2DWait%2DTimes.ipynb) in Jupyter Notebook, JupyterLab, or Google Colab.
3. Install the Python libraries imported by the notebook, including NumPy, pandas, Matplotlib, Plotly, and scikit learn.
4. Select Restart & Run All to generate the analyses and visualizations.
Note: Running the notebook requires internet access to retrieve the CSV files from the team repository. Some interactive Plotly maps may render differently depending on the environment.
Recommendations
Based on the notebook's analyses, the team recommended prioritizing capacity and faster patient flow at overloaded emergency departments, improving transfer and behavioral health pathways, and benchmarking hospitals against facilities with similar ED volumes rather than relying on overall hospital star ratings alone.
Limitations
1. The findings are observational and do not establish causation.
2. Some hospitals are missing ED volume, wait time, or star rating data.
3. ED wait times and other CMS measures cover somewhat different reporting periods.
4. Census economic indicators are measured at the state level rather than in each hospital's local community.
5. Estimated patient improvements are hypothetical and would need validation through operational pilots.
Team and Acknowledgments
Cohort A, Team 4: Hassan Imran Malik, Aashna Pathi, Michael Lee, and Weiran Wang.

This repository presents a collaborative course project. My primary contribution was the patient experience analysis.

For complete charts, methodology, source references, team contributions, and the project's generative AI disclosure, please refer to the notebook.
