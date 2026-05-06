# Medical Appointment No-Show Analysis

## Description
I completed this project as part of Udacity's Data Analyst nanodegree program. This project shows my ability to use pandas to go through the data analysis process. The analysis uses data from Kaggle ([original source](https://www.kaggle.com/datasets/joniarroba/noshowappointments)) on medical appointments in Brazil, and it uncovers interesting correlations in the data.

## Dataset
The dataset contains information on over 110,000 scheduled medical appointments from public hospitals in Brazil, with patient demographics, appointment timing, health indicators, and a label indicating whether the patient showed up or not. Key variables include age, gender, appointment and scheduling dates, hospital neighborhood, participation in the Bolsa Família welfare program, several chronic conditions, whether an SMS reminder was received, and the no‑show flag.​

## Questions Explored
The notebook is organized around three main analytic questions:​
- Is there a correlation between the patient's age and whether or not the appointment is a no-show? If so, what is the correlation?
- Is there a correlation between how many days in advance an appointment is scheduled and whether or not the appointment is a no-show? If so, what is the correlation?
- Do some hospitals have higher no-show rates than others?

## Data Wrangling and Cleaning
The project performs several cleaning and preparation steps before analysis:​
- Converts scheduling and appointment timestamps to dates and computes a new DaysInAdvance feature.​
- Removes records where the scheduled date is later than the appointment date, which indicate invalid entries.​
- Identifies and drops a single record with an age of −1, treating it as a data error, and keeps the rest of the records which all have valid ages.

## Analysis and Methods
Using pandas the notebook:​
- Splits the dataset into show and no‑show groups and compares summary statistics for age and days scheduled in advance.​
- Creates histograms of the number of no-show appointments and no‑show percentages by age and by how many days in advance an appointment was scheduled to visualize patterns.​
- Aggregates data by hospital neighborhood to compute no‑show rates and highlights neighborhoods with especially high or low rates.​
- No formal hypothesis tests are applied; findings are framed as correlations rather than causal conclusions.​

## Key Findings
- Age appears to have a non‑linear relationship with no‑show rates, with babies/young children and adults in their mid‑50s to mid‑70s less likely to miss appointments than some middle‑age groups.​
- Appointments scheduled very close to the appointment date (e.g., within about a week) have substantially lower no‑show rates than those scheduled a couple of weeks in advance.
- Some hospitals (for example, hospitals in Santa Cecília and Santos Dumont) have no‑show rates of over one‑quarter of appointments, while at least one hospital has notably lower rates and shorter scheduling lead times.​

These patterns are treated as suggestive and not as evidence of causality.​

## Limitations and Future Work
The analysis has several important limitations:​
- It does not include statistical tests or confidence intervals, so the strength and significance of observed patterns are not formally quantified.​
- There is limited data for some groups, such as patients with high ages and hospital in some neighborhoods.​

Potential next steps to extend the project include:​
- Applying statistical tests or simple models to quantify the association between features and no‑shows.​
- Exploration associations between other features (such as health conditions and SMS reminders) and no-shows.​
- Investigating operational or policy interventions for high no‑show neighborhoods, informed by more detailed modeling and domain knowledge.​

## Technologies Used
Python, Jupyter Notebook, pandas, NumPy.​

## How to Run
1. Clone this repository and download the CSV file from [Kaggle](https://www.kaggle.com/datasets/joniarroba/noshowappointments) into the same directory as the notebook.​
2. Ensure pandas and NumPy are installed.​
3. Open the notebook in Jupyter and run all cells from top to bottom.
