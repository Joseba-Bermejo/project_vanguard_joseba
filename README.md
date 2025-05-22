# Vanguard A/B Test – Client Experience Redesign Analysis

## Project Overview

This analysis investigates the results of an A/B test run by Vanguard, a US-based investment management company, to evaluate whether a redesigned user interface improved client experience on their digital platform. The experiment aims to determine whether these changes led to higher completion rates, fewer errors, and better client outcomes.

---

## Data Description

The analysis uses three core datasets:

- **Client Profiles (`df_final_demo`)**  
  Contains demographic details such as age, gender, number of accounts, and balance.

- **Digital Footprints (`df_final_web_data`)**  
  Captures user journey data through various online steps, including timestamps and user actions. It is divided into pt_1 and pt_2 and must be merged.

- **Experiment Roster (`df_final_experiment_clients`)**  
  Assigns users to either the control group (traditional interface) or test group (new design).

### Key Fields

- `client_id`: Unique identifier for each client  
- `variation`: Indicates control vs. test group  
- `visit_id`: Unique session ID  
- `process_step`: The online process step  
- `clnt_age`: Age of the client  
- `gendr`: Gender  
- `logons_6_mnth`: Logins in the past 6 months  
- `calls_6_mnth`: Calls made in the past 6 months  
- `clnt_tenure_yr`: Years the client has been with Vanguard  
- `bal`: Account balance  
- `date_time`: Timestamp of user activity

---

## Project Structure

This analysis was built following these steps:

### 1. Data Cleaning & EDA
- Merged and cleaned raw datasets
- Analyzed client demographics and behavior

### 2. Performance Metrics
- **Completion Rate**: % of visits who reached the confirm step
- **Time Spent on Each Step**: Average time per step
- **Error Rate**: % of visits who returned to earlier steps
- **Error Criticality**: % of visits with error that didn't reach the confirm step

### 3. Hypothesis Testing
- **1. Main Hypothesis**: The new design results in a significantly higher completion rate
- **2. Cost-Effectiveness Test**: Does the improvement meet the 5% threshold?
- **3. Error Rate Test**: Does the new design result in less errors?
- **4. Error Criticality Test**: Is the error criticality lower in the new design?

### 4. Experiment Evaluation
- Checked for randomization issues or design bias
- Assessed experiment duration sufficiency
- Identified additional data needs (e.g., user feedback, contextual info)

---

## Key Insights & Conclusions

- Completion Rate increased 8.7% in the new design
- Error Rate increased 6.5% in the new design
- Error Criticality increased 10.8% in the new design
- ***Recommendation: Not rolling out the new design at this time due to increased error criticality, despite the improvement in completion rate.***

---

## Tools Used

- **Python**: Pandas, Seaborn, Matplotlib, SciPy, Statsmodels  
- **Tableau**: Interactive dashboards, KPIs and A/B test visualizations  
- **Git & GitHub**: Version control and project repository  
- [**Trello**: Kanban board for project management](https://trello.com/b/uIXXZXB7/projectvanguard)
