# Insurance Claims Fraud Analysis – Orange Data Mining

A no-code exploratory analysis of an insurance claims dataset to find which claim characteristics are associated with reported fraud.
Module 8 mini-project for **AAI101 Introduction to AI** (DMACC, Fall 2026), by Patrick Hall.

## The question
Which claims should an insurer look at more closely? I compared fraud and non-fraud claims by claim amount, time of day, and incident severity.

## What I did
- Loaded the course-provided `Insurance.csv` (1,000 claims, 69 columns, no missing values) with the **File** widget and set `fraud_reported` as the target.
- Built a workflow in **Orange Data Mining** that feeds one File widget into **Data Table**, **Distributions**, **Scatter Plot**, and **Box Plot**.
- Compared group means with Orange's **Student's t-test** and broke out fraud rates by incident severity.

## Key findings
| Finding | Result |
|---|---|
| Overall fraud rate | 247 of 1,000 claims (24.7%) |
| Average claim, fraud vs. non-fraud | $60,302 vs. $50,288 (t-test p < 0.001) |
| Time of day | No visible pattern; fraud appears at every hour |
| Major-damage claims | 167 of 276 were fraud (60.5%) |
| Other severity levels | 6.7%–12.9% fraud |

**Takeaway:** flag major-damage and larger claims for closer **human review**. Neither one proves fraud on its own.

## Files
- [`docs/Insurance_Fraud_Analysis_Orange.pdf`](docs/Insurance_Fraud_Analysis_Orange.pdf): the full write-up with workflow screenshots and interpretation
- [`screenshots/`](screenshots/): installation, workflow, and chart screenshots

The dataset was provided by the course and is not redistributed here.

## Skills shown
Data analysis workflow design, descriptive statistics (mean, median, standard deviation), hypothesis testing (t-test), data visualization, insurance-domain interpretation, and clear documentation.

*Note: as stated in the write-up, AI was used for proofreading and formatting.*
