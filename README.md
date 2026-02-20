<img width="851" height="572" alt="image" src="https://github.com/user-attachments/assets/94e288d2-1392-4886-b627-4ee66e2ec8b2" />


# Financial Loan Performance & Risk Analysis

## Project Purpose
This project analyzes a financial institution's loan dataset to understand how customers borrow, repay, and default on loans.
The goal is to transform raw transactional data into meaningful insights that help management make better lending decisions, reduce losses, and approve the right customers.
In simple terms, the analysis answers:
* Are we lending money safely?
* * Who is most likely to repay?
Who is most likely to default?
* What rules should the company change?



## What the Analysis Is About
Financial organizations do not fail because they lack customers - they fail because they lend to the wrong customers.
This analysis evaluates:
* Loan performance
* Customer financial strength
* Behavioral patterns
* Risk drivers
* Profitability indicators
The project converts raw loan records into a decision-making dashboard that management can use to adjust lending policies.

## Problem Statement
The company possesses detailed loan records but lacks a clear understanding of:
* Which customers are risky
* Why defaults occur
* How loan characteristics influence repayment
* Whether the portfolio is healthy or deteriorating
Without this knowledge, lending decisions rely on assumptions rather than evidence, increasing financial risk.

## Objectives
The objectives of this analysis are:
* Measure the size and health of the loan portfolio
* Identify patterns affecting loan repayment
* Detect high-risk customer groups
* Understand drivers of default
* Provide data-driven lending recommendations
* Build an interactive dashboard for business users

## Data Preparation & Cleaning
### Tool used:power BI
Raw datasets rarely come ready for analysis.
Several transformations were necessary before meaningful analysis could begin:

## Key Cleaning Steps
* Corrected data types (dates, numbers)
* Created a date table for trend analysis
* Removed inconsistencies
* Created calculated columns for segmentation
* Built business measures using DAX
The most important transformation involved the employment length column.

## Special Data Treatment - Employment Length Conversion
* The Problem
The employment length column did not contain exact numbers.Instead it contained categories such as:
"< 1 year"
"2 years"
"7 years"
"10+ years"
This is not numeric data - it is grouped information.
But calculations such as average employment length require numbers.

## Why We Cannot Just Guess
So statistical approach was used.

## Statistical Approach Used
* Step 1 - Handling "Less Than 1 Year"
This value lies between 0 and 1 year.
Since the exact value is unknown, the best estimate is the midpoint:
(0 + 1) ÷ 2 = 0.5 years
This gives the most balanced estimate without favoring low or high values.

* Step 2 - Handling "10+ Years"
This value has no upper limit, so a midpoint cannot be directly calculated.
Instead, we reconstruct the likely range.
All other categories increase in 1-year steps:
1 year, 2 years, 3 years … 9 years
So the final group logically continues for a few similar steps:
10 to 14 years (typical long-tenure range)

* Now midpoint can be estimated:
(10 + 14) ÷ 2 = 12 years

* Why This Matters
Using 10 instead of 12 reduces the calculated average tenure and makes customers appear riskier than they actually are.
Statistical estimation prevents misleading business conclusions.

### Layman Explanation
We did not change the data - 
we estimated the most realistic value inside a range.

### Think of it like age groups:
If someone says "between 20 and 30 years old,"
we do not record them as 20 or 30.
We record the middle - about 25.
That is exactly what was done for employment duration.

## Feature Engineering (New Columns Created)
To make patterns easier to detect, raw numbers were grouped into meaningful business categories:
* Income groups
Debt burden levels
* Employment stability levels
* Loan size categories
* Interest rate bands
* Credit experience groups
This allows comparison between customer types instead of individual records.

## Analytical Method
The analysis followed a business-style workflow:
* Step 1 - Portfolio Overview
Measure total loans and distribution
* Step 2 - Performance Evaluation
Compare good vs bad loans
* Step 3 - Trend Analysis
Check if loan quality changes over time
* Step 4 - Risk Segmentation
Identify dangerous customer groups
* Step 5 - Root Cause Analysis
Determine why defaults happen

## KPI IMPORTANCE
### Total Loans
* 👉 Measures lending activity and portfolio size
 ✔ Shows demand
 ✔ Indicates market reach
* Business meaning:
If loans increase → growth
 If loans drop → reduced lending confidence

### Total Loan Amount
* 👉 Shows financial exposure
* Business meaning:
 Higher amount = higher profit potential but also higher risk

###  Average Loan Size
* 👉 Reveals borrower behavior
* Business meaning:
High average → large exposure per customer
Low average → diversified risk

### Default Rate (Most Important KPI)
* 👉 Measures portfolio risk
* Business meaning:
High default → poor lending quality
Low default → strong credit policy
This KPI drives most business decisions.

## KPI Overview Values
* Total Loans: 38.6K
* Total Loan Amount: $435.8M
* Average Loan Size: $11.3K
* Default Rate: 13.8%

* Insight:
The portfolio is large and profitable, but a 13.8% default rate is high in lending standards (healthy range is usually <10%).This means risk management policies need improvement.

# PAGE 1 - LOAN PORTFOLIO OVERVIEW
* (Where money went)




<img width="1337" height="759" alt="image" src="https://github.com/user-attachments/assets/9741826d-a396-4a06-9c60-e190f9204a9b" />


## Key Insights
### ✅ Majority of loans are concentrated in Debt Consolidation
 * 👉 Indicates customers use loans to manage existing debt
### ✅ Grade B & C dominate total loan amount
 * 👉 Suggests institution targets moderate-risk borrowers
### ✅ 60-month loans hold the largest share
* 👉 Customers prefer longer repayment periods
### ✅ Certain states (CA, NY, TX) receive highest funding
 * 👉 Geographic concentration risk exists


## Recommendations
* Diversify lending across states
* Monitor debt consolidation loans closely (possible hidden risk)
* Review long-term loan risk exposure



# PAGE 2 - LOAN PERFORMANCE ANALYSIS
* (Are we safe?)




<img width="1342" height="756" alt="image" src="https://github.com/user-attachments/assets/e9ad88b4-d97b-405b-a573-570228eae795" />


## Key Insights
### ✅ Fully Paid loans dominate portfolio
* 👉 Positive repayment behavior
### ✅ Default rate increases sharply from Grade D → G
* 👉 Credit grading is working effectively
### ✅ 60-month loans show slightly higher default
* 👉 Longer terms increase risk
### ✅ Early career borrowers show more defaults than experienced borrowers


## Recommendations
* Tighten approval criteria for Grades E–G
 * Introduce stricter checks for long-term loans
 * Consider employment stability in approval decisions


# PAGE 3 - TREND ANALYSIS
* (Are we improving?)



<img width="1337" height="745" alt="image" src="https://github.com/user-attachments/assets/d1f8c53b-e12e-4435-949f-b4e13ac1597c" />



## Key Insights
### ✅ Loan issuance increases steadily throughout the year
 * 👉 Portfolio expansion
### ✅ Default rate fluctuates but slightly trends upward toward year-end
 * 👉 Risk rising alongside growth


## Recommendations
* Monitor seasonal default spikes
* Strengthen underwriting during peak lending months
*  Balance growth with risk management


# PAGE 4 - RISK & PROFITABILITY INDICATORS
* (Who is dangerous?)




<img width="1338" height="748" alt="image" src="https://github.com/user-attachments/assets/151848c7-c167-46d9-899a-fb56ab8079d0" />

## Key Insights
### ✅ Low-income customers have highest default rate
* 👉 Income is a strong risk driver
### ✅ Grades F & G exhibit very high default probability
 * 👉 Risk segmentation confirmed
### ✅ Higher interest loans correlate with higher default (scatter plot insight)
 * 👉 Risk-based pricing alone does not offset default risk


## Recommendations
* Adjust pricing for high-risk borrowers
* Introduce risk-based credit limits
* improve income verification for low-income borrowers


# PAGE 5 - CUSTOMER & LOAN PROFILE ANALYSIS
* (Ideal customer)



<img width="1343" height="740" alt="image" src="https://github.com/user-attachments/assets/b26d5cc7-aeee-4035-9426-d7ed16098057" />

## Key Insights
### ✅ Very high-income customers show lowest default
 * 👉 Strong repayment ability
### ✅ Experienced & veteran workers demonstrate better loan performance
 * 👉 Employment stability reduces risk
✅ Debt consolidation dominates purpose across all income groups


💡 Recommendations
✔ Target high-income experienced customers
 ✔ Develop tailored products for stable workers
 ✔ Monitor debt consolidation for hidden financial stress



# KEY INFLUENCERS VISUAL (EXPLANATION)



<img width="668" height="542" alt="image" src="https://github.com/user-attachments/assets/4c9efa97-5aba-40af-a4f0-a04ef4defb29" />

* The Key Influencers chart answers:
👉 What factors increase default rate?

* What my visual shows
The Key Influencers visual identifies the strongest drivers of default. It shows that lower credit grades and longer loan terms significantly increase the likelihood of loan failure, helping management focus risk mitigation strategies on the most dangerous segments.

### Top drivers increasing default:
* Grade G → strongest default driver
* House loan purpose → higher risk
* Grade F → high risk
* 60-month term → risk increase
* Grade E → moderate risk

### Why this visual is powerful
It uses machine learning logic to:
 ✔ Detect hidden risk patterns
 ✔ Rank drivers by impact
 ✔ Show probability of risk increase

# SCATTER PLOT EXPLANATION




<img width="337" height="552" alt="image" src="https://github.com/user-attachments/assets/647824c2-3029-4d86-962b-ef47a702555c" />

The scatter plot shows relationship between:
Interest rate
Loan amount
Loan status

The scatter plot reveals the relationship between pricing and risk. It helps identify whether higher interest rates effectively compensate for increased default risk and highlights segments where large loan exposure coincides with poor repayment performance.
What it reveals
I detected:
✔ High interest + high default = risky pricing strategy
 ✔ Low interest + low default = safe customers
 ✔ Large loans with default = high exposure risk


# BUSINESS STORY OF MY DASHBOARD
My dashboard shows:
✔ Lending activity is growing
 ✔ Credit grading effectively segments risk
 ✔ Income and employment stability strongly influence repayment
 ✔ Longer loan terms increase default probability
 ✔ Debt consolidation dominates borrowing behavior
 ✔ High-risk grades require stricter controls

# Key Business Value
This analysis helps management:
* Reduce default risk
* Improve approval policies
* Target safer customers
* Adjust interest pricing
* Monitor loan health continuously

# Final Business Recommendation
The company should shift from volume‑based lending to risk‑adjusted lending by combining customer affordability indicators, loan characteristics, and historical repayment behavior to guide approvals. This approach reduces losses while maintaining long‑term profitability.
Conclusion
This project demonstrates that proper data preparation is as important as visualization.
Incorrect assumptions in preprocessing can distort results and lead to poor financial decisions.
Using statistical reasoning ensures fair representation of customers and reliable insights.
The final dashboard transforms raw loan records into a decision-support tool that guides responsible lending .
