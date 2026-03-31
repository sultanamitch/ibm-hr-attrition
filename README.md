# IBM HR Analytics — Employee Attrition Analysis

## Overview

I analyzed IBM employee attrition data to figure out why people leave. What I found was when I looked at the effort required for an IBM employee to do their job — overtime, business travel required — I saw that the more effort required from IBM employees to do their job, the higher attrition I saw. This data shows us that if IBM can lower the effort required for IBM employees to do their job, IBM can keep talent and reduce the risk of needing to replace employees and onboard new ones.

Next, I saw that career growth has a direct impact on attrition. If IBM employees receive promotions when deserved I saw lower attrition, and when IBM employees stay at IBM longer they tend to stay employed longer, reducing attrition.

When I looked at performance ratings at IBM I noticed the data was not fully reliable and was limited in the sense that the scale was 1 through 4, but the only recorded scores range from 3-4. I can observe this may be due to managers not being willing to hand out lower scores in fear it would reflect poorly on them. This requires more data to fully understand.

When I analyzed employee satisfaction I saw that IBM employees with higher job involvement scores had lower attrition rates — a pretty wide delta — with scores of 1 showing a 33.7% attrition rate vs 9.0% for ratings of 4.

I also looked at employee profiles. IBM employee profiles pointed to my theory of life stage and survivorship bias. I saw this in marital status, job level, and age. Sales representatives at IBM have the highest attrition rate of any role at 39.8%, which is consistent with the nature of sales positions and their historically high turnover.

Based on this analysis, I recommend IBM prioritize three areas: auditing overtime and travel requirements for high-attrition roles, implementing structured promotion timelines for employees in the 6-10 year tenure window, and improving job involvement through clearer role ownership and career pathing.

---

## Business Question

What factors drive employee attrition at IBM, and what operational changes would reduce it?

---

## Dataset

- Source: IBM HR Analytics Employee Attrition & Performance (Kaggle)
- 1,470 employees, 35 columns
- Attrition is defined as the employee is no longer at IBM — voluntary resignation, termination, and retirement are not distinguished

---

## What I Did

I downloaded the IBM employee attrition dataset from Kaggle to understand what drives employee turnover and identify patterns in the data and loaded it into a pandas DataFrame. I then cleaned the data by dropping constant columns and binary encoding the Attrition variable, then stored it in a SQLite database so I could query it efficiently. I wrote SQL queries to calculate attrition rates across key variables like overtime status, job level, department, marital status, and job role then built bar charts in matplotlib to visualize the patterns as I went. I documented my findings and interpretations directly in the notebook as each analysis was completed in markup sections within my notebook, which let me spot patterns and adjust my next questions. Then I built an interactive two-page dashboard in Tableau Public to present the full analysis.

**[View Dashboard on Tableau Public](https://public.tableau.com/app/profile/mitch.sultana/viz/Book1_17743316025170/WorkforceEffortFactors)**

---

## Strongest Findings

- Overtime employees leave at 30.5% vs 10.4% — nearly 3x higher
- Frequent business travelers leave at 24.9% vs 8.0% for non-travelers
- Sales Representatives have the highest attrition of any job role at 39.8%
- Employees with low job involvement (score 1) leave at 33.7% vs 9.0% for score 4
- Single employees leave at 25.5% vs 10.1% for divorced employees
- Entry-level employees (Job Level 1) leave at 26.3% vs 4.7% for managers

---

## Tools

Python, pandas, SQLite, matplotlib, Jupyter Notebook, Tableau Public, Git

---

## Other Projects

- [Friction-First: Tech Sector Earnings Screener](https://github.com/sultanamitch/friction-first-screener)
- [Energy Project Screening (CAISO Queue Analysis)](https://github.com/sultanamitch/energy-project-screening)
