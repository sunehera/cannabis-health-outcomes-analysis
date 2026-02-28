# Cannabis Health Outcomes Analysis
### 2024 Canadian Cannabis Survey — Exploratory Analysis & Predictive Modeling

---

## Overview
This project analyzes self-reported health outcomes and cannabis usage 
patterns among 3,551 cannabis users from the 2024 Canadian Cannabis 
Survey (Statistics Canada), a nationally representative sample of 
11,666 Canadians aged 16+.

The central research question is: **What factors predict whether 
someone uses cannabis for medical versus recreational purposes?**

This analysis was motivated by the growing need for rigorous 
computational approaches to understanding therapeutic cannabis 
outcomes — an area of active research at institutions like the 
Johns Hopkins Cannabis Science Laboratory and through large-scale 
observational studies like the National Cannabis Study.

---

## Data Source
- **Dataset:** 2024 Canadian Cannabis Survey Public Use Microdata File
- **Publisher:** Statistics Canada
- **Respondents:** 11,666 adults aged 16+ across all Canadian provinces
- **Access:** Publicly available at open.canada.ca

---

## Project Structure
```
cannabis-health-outcomes-analysis/
│
├── README.md
├── 01_exploratory_analysis.ipynb   
├── 02_predictive_modeling.ipynb    
└── data/
    └── ccs_pumf_2024-002.csv
```

---

## Key Findings

### Finding 1 — Age and Purpose of Use
Cannabis use for medical purposes increases significantly with age.
Users aged 45-54 and 55+ show notably higher rates of medical use
compared to younger age groups, consistent with higher prevalence
of chronic conditions in older populations.

### Finding 2 — Route of Administration
Oils/tinctures and topical application are notably more common among
medical users, reflecting their use for precise dosing and localized
pain relief. Concentrate use is nearly identical between non-medical
(4.2%) and medical users (4.4%), suggesting high-potency products
serve distinct but equally compelling purposes across user types.

### Finding 3 — Symptom Profiles Differ Between User Groups
Medical-only users show higher rates of serious physical conditions:
chronic pain (36.7%), arthritis (39.4%), cancer (2.7%). Dual-purpose
users show higher rates of mental health conditions: anxiety (32.3%),
depression (30.4%), ADHD (20.2%). Sleep problems are the most
prevalent condition across both groups (~44-48%).

### Finding 4 — Knowledge Gaps About Cannabis
Only 65.9% of medical-only users correctly know edibles can take up
to 4 hours to take effect. Fewer than 13% of users across all groups
understand THC potency and impairment correctly. These knowledge gaps
have direct implications for patient education and harm reduction.

### Finding 5 — Health Status
Medical users report the poorest physical health — 32.1% fair or poor
vs 12.3% of non-medical users. Surprisingly, the dual-purpose group
reports the worst mental health (14.2% poor), consistent with their
higher rates of anxiety and depression.

### Finding 6 — Predictive Model
A logistic regression model predicts medical vs recreational cannabis
use with 71% accuracy and AUC of 0.755 using only demographic, health,
route of administration, and belief variables. The three strongest
predictors are all route of administration variables — topical use
(coef: 1.59), oil use (coef: 1.38), and concentrate use (coef: 0.53)
— suggesting HOW people consume cannabis is more predictive of medical
intent than WHO they are demographically.


---

## Methods
- **Language:** Python 3.9, R
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn
- **Models:** Logistic Regression, Random Forest (with class balancing)
- **Evaluation:** Accuracy, Precision, Recall, F1, ROC-AUC

---

## Author
**Sunehera Hasib**
B.Sc. Computational and Data Science, George Mason University
shasib@gmu.edu
