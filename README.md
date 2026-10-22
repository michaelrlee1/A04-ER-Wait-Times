What Drives Emergency Department Wait Times Across U.S. Hospitals?
A data analytics project examining why emergency department (ED) wait times differ across U.S. hospitals and how those delays affect patients.

Course: BA780 — Boston University, Questrom School of Business
Project: A04 / Final Project · Cohort A, Team 4
Tools: Python, pandas, NumPy, Matplotlib, Plotly, scikit-learn, Jupyter Notebook
Project Overview
Emergency department wait times vary significantly across the United States. This project analyzes 4,080 hospitals to explore the relationship between ED wait times and hospital volume, patient flow, hospital characteristics, and state economic conditions.

Using public data from the Centers for Medicare & Medicaid Services (CMS) and the U.S. Census Bureau, our team combined three datasets, cleaned and merged the records, created visualizations, and used correlation analysis and linear regression to identify patterns that could inform hospital operations decisions.

Main measure: OP_18b — median time spent in the ED, from arrival to departure, excluding psychiatric and transfer patients.
Key Questions
- Are busier emergency departments associated with longer wait times?
- How do wait times relate to patients leaving before receiving care?
- Which patient groups experience the longest stays?
- How do hospital ownership, quality ratings, and rural status relate to wait times?
- Do state economic conditions help explain differences in ED performance?
Key Findings
Finding	Result
ED volume and wait time	Median visits increase from 120 minutes in low-volume EDs to 192.5 minutes in very-high-volume EDs.
Patients leaving without being seen	The average share rises from 0.70% at hospitals with median visits under two hours to 3.91% at hospitals over four hours — approximately 5.6 times higher.
Correlation with walkouts	Median ED time and the percentage leaving before being seen show a positive correlation of 0.52.
Psychiatric and transfer patients	At very-high-volume EDs, the slowest quarter reports median psychiatric stays of 368 minutes, compared with approximately 222 minutes at the fastest quarter.
Hospital ratings	Overall hospital star ratings explain less than 1% of the observed variation in ED wait times in the notebook's comparison.
State comparison	Massachusetts has a median ED time of 211.5 minutes, compared with 126 minutes in Minnesota; differences in ED size and rural hospital mix help explain this gap.


These are observational associations, not proof that any one factor causes longer waits.
My Contribution — Patient Experience Analysis
I worked on the project's patient-focused analysis (Part 2; Charts 9–10), examining how longer ED stays are associated with patients leaving without being seen, and comparing psychiatric and transferred-patient wait times across ED volume groups and states.

This included:
- Grouping hospitals by median ED duration and comparing the percentages of patients who left before receiving care.
- Examining the relationship between ED duration and patients leaving without being seen.
- Comparing psychiatric and transferred-patient stays across ED volume categories.
- Exploring differences in psychiatric wait-time gaps among states.
- Estimating potential patient-level improvements under benchmark-based scenarios.
Patient impact: The analysis estimated that approximately 116,338 additional patients per year could remain to be seen if 142 very-high-volume EDs with median visits over four hours reduced their walkout rates to those observed in the 3–4-hour group. This is a scenario estimate, not a validated forecast.
Data Sources
1. CMS — Timely and Effective Care, Hospital: ED wait-time metrics, ED volume, and patients leaving without being seen.
2. CMS — Hospital General Information: hospital characteristics, ownership, and overall star ratings.
3. U.S. Census Bureau — 2024 ACS 1-Year, Table DP03: state-level income, employment, insurance, and commuting statistics.
The notebook retrieves the three CSV files from our team's data repository.
Methods and Tools
- Data preparation: Reshaped CMS measures, converted missing-value strings into NaN, preserved hospital IDs as text, and merged the hospital and Census data.
- Exploratory data analysis: Summaries and comparisons by hospital size, ownership, patient category, and state.
- Visualization: Histograms, bar charts, scatter plots, and U.S. choropleth maps.
- Statistical analysis: Correlations, within-group comparisons, and state-level linear regression.
How to Run the Project
1. Download or clone this repository.
2. Open the notebook, [`FInal A04-What-Drives-ER-Wait-Times.ipynb`](FInal%20A04-What-Drives-ER-Wait-Times.ipynb), in Jupyter Notebook, JupyterLab, or Google Colab.
3. Install the Python packages if needed:
   pip install numpy pandas matplotlib plotly scikit-learn nbformat jupyter
4. Select Restart & Run All to generate the analyses and visualizations.
Note: Running the notebook requires internet access to load the CSV files from the team repository. Some interactive Plotly maps may render differently depending on the notebook environment.
Recommendations
Based on the notebook's analyses, the team recommended prioritizing capacity and faster patient flow at overloaded EDs, improving transfer and behavioral-health pathways, and benchmarking hospitals against others with similar ED volume rather than using overall star ratings alone.
Limitations
- The findings are observational and do not establish causation.
- Some hospitals are missing ED volume, wait-time, or star-rating data.
- ED wait times and other CMS measures cover somewhat different reporting periods.
- Census economic indicators are measured at the state level rather than the hospital's local community.
- Estimated patient improvements are hypothetical and would need validation through operational pilots.
Team and Acknowledgments
Cohort A · Team 4: Hassan Imran Malik, Aashna Pathi, Michael Lee, and Weiran Wang.
This repository presents a collaborative course project; my primary contribution was the patient experience analysis.

For complete charts, methodology, source references, team contributions, and the project's generative AI disclosure, see the notebook.
