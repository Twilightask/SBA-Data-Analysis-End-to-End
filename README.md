SBA Loan Portfolio Risk & Lending Analytics
End-to-End Data Analytics Project | Excel • MySQL • Power BI

An end-to-end analytics project analysing a large U.S. Small Business Administration (SBA) loan portfolio to identify patterns in loan defaults, financial losses, borrower characteristics, sector performance, geographic risk, bank performance, and lending trends.

The project combines data cleaning, SQL-based business analysis, risk analysis, customer segmentation, and interactive Power BI reporting to translate historical loan data into actionable insights for portfolio and lending risk management.

Business Question:
What borrower, loan, sector, and geographic characteristics should be considered when assessing historical lending risk?

📌 Project Overview

This project analyses approximately 899K SBA loan records across multiple dimensions including:

Sectors / Industries
States and Cities
Employee Categories
Business Type
Loan Amount
Loan Term
SBA Guarantee / Coverage
Banks
Loan Status
Time Periods

The analysis focuses on understanding:

Where defaults are concentrated
Where financial losses are highest
Which borrower characteristics are associated with higher default rates
Which industries and states carry greater historical risk
How loan characteristics relate to repayment outcomes
How banks differ in portfolio performance
How borrower characteristics combine to create different risk profiles
How portfolio performance changed over time

The final findings are presented through an interactive 4-page Power BI dashboard.

🎯 Business Objectives

The project was designed to answer key lending and portfolio-risk questions:

Which states have the highest lending exposure and charged-off amounts?
Which industries have the highest and lowest observed default rates?
Which industries contribute the greatest financial losses?
Does employee size influence repayment performance?
Do new businesses show higher default rates than existing businesses?
Does loan term affect historical default risk?
Which loan amount ranges show higher observed default rates?
Does SBA guarantee coverage show a relationship with default rates?
Which combinations of borrower characteristics are associated with higher risk?
Which banks demonstrate stronger or weaker historical portfolio performance?
How did lending activity and portfolio risk change over time?
How did portfolio performance differ around the 2008 financial crisis period?
How can historical borrower characteristics be used to support risk screening?
🛠️ Tools & Technologies
Tool	Purpose
Excel	Data cleaning, validation and feature preparation
MySQL	Exploratory analysis, business analysis and risk analysis
Power BI	Interactive dashboards and visualization
DAX	Dashboard measures and calculated metrics
GitHub	Project documentation and portfolio presentation
🔄 End-to-End Workflow
Raw SBA Dataset
       ↓
Excel
Data Cleaning & Validation
       ↓
MySQL
Business & Risk Analysis
       ↓
Derived Metrics & Segmentation
       ↓
Power BI
Interactive Dashboard
       ↓
Business Insights
       ↓
Recommendations
🧹 Data Preparation

The dataset was cleaned and validated before analysis.

Key preparation activities included:

Handling missing business-state information
Standardizing state names
Handling missing bank information
Standardizing categorical fields
Investigating inconsistent approved/disbursed amounts
Correcting identified date inconsistencies
Converting financial fields into appropriate numeric formats
Standardizing loan-status values
Creating analysis-ready categorical features
Derived Features

Several features were created to simplify business analysis and improve interpretability:

Sector
Loan Category
Loan Term Category
Employee Category
Business Type
SBA Coverage Category
SBA %
Charged-Off Category

These features were created using transparent, rule-based categorisation rather than replacing the original source fields.

📊 Key Metrics
Default Rate
Default Rate =
Defaulted Loans / Total Loans

Measures the proportion of loans that resulted in default.

Loss Rate
Loss Rate =
Charged-Off Principal / Loan Amount Disbursed

Measures the proportion of disbursed lending exposure that resulted in charged-off principal.

SBA Guarantee %
SBA Guarantee % =
SBA Guaranteed Amount / Approved Amount

Measures the level of SBA guarantee relative to the approved amount.

Average Loan Amount

Average disbursed loan amount across the portfolio.

🔎 SQL Analysis

MySQL was used to perform the core business and risk analysis.

Portfolio Analysis
Total loan volume
Approved amount
Disbursed amount
SBA guaranteed amount
Default rate
Loss rate
Average loan amount
Portfolio growth
Sector Analysis
Sector loan volume
Sector exposure
Default rate by sector
Loss rate by sector
Charged-off principal by sector
SBA guarantee percentage by sector
Sector risk ranking
Geographic Analysis
State loan volume
State exposure
State default rate
State charged-off amounts
State performance scorecards
State → Sector risk analysis
Borrower Analysis
Default rate by employee category
New vs Existing business performance
Business type analysis
Employee category scorecards
Customer persona analysis
Loan Analysis
Default rate by loan category
Default rate by loan term
Loan amount analysis
SBA coverage analysis
Bank Analysis
Banks ranked by loan volume
Banks ranked by approved amount
Bank default rates
Bank loss rates
Bank performance comparisons
Advanced SQL Analysis

The project also used:

CTEs
Window functions
Rankings
Conditional aggregation
Multi-dimensional segmentation
Customer personas
Performance scorecards
📈 Power BI Dashboard

The final Power BI report contains four analytical pages.

1️⃣ Portfolio Overview

Provides an executive-level view of:

Total loans
Total disbursed amount
Total approval amount
Total SBA guaranteed amount
Defaulted loans
Default rate
Average loan amount
Average SBA guarantee %
Business-type distribution
Geographic distribution
Employee-category distribution
Business Purpose

Provides a high-level view of portfolio scale, funding, borrower mix and overall credit performance.

2️⃣ Sector & Borrower Risk Analysis

Focuses on sector-level risk and loan characteristics.

Key analyses include:

Loan volume by sector
Disbursed amount by sector
Sector loss rate
Sector default rate
Loan-term risk
Sector loan volume vs default rate
Highest-risk sectors
Business Purpose

Identifies industries and loan characteristics associated with higher historical credit risk and financial losses.

3️⃣ State & Geographic Loan Analysis

Focuses on geographic portfolio performance.

Key analyses include:

Default rate by state
State loan volume
SBA guarantee coverage by state
Top states by lending exposure
State disbursed amount vs average loan amount
State → sector risk drivers
Default rate and loan volume over time
Loan amount band risk
Business Purpose

Helps identify geographic concentration, state-level risk and exposure patterns.

4️⃣ Loan & Borrower Risk Analysis

Focuses on borrower characteristics and financial impact.

Key analyses include:

Default rate by employee size
Default rate by business type
Default rate by SBA coverage level
Industry risk vs financial loss
Charged-off principal by industry
Business Purpose

Moves the analysis closer to the lending decision by examining which borrower and loan characteristics are associated with historical risk.

💡 Key Business Insights
1. Portfolio Credit Risk Is Material

The portfolio contains approximately 899K loans with an observed default rate of 17.55%.

This demonstrates why portfolio growth should be evaluated together with credit-risk indicators rather than using loan volume alone.

2. Self-Employed Borrowers Show Higher Observed Default Rates

The Self-Employed employee category has an observed default rate of approximately 22.80%, considerably higher than several larger employee categories.

This suggests that business size can be a useful historical risk indicator when combined with other borrower characteristics.

3. New Businesses Show Higher Default Rates

Observed default rates in the Power BI analysis were approximately:

Business Type	Default Rate
New	18.74%
Existing	17.10%
Unknown	7.09%

New businesses therefore show a higher observed default rate than existing businesses in this portfolio.

4. SBA Coverage Levels Show Significant Differences in Default Rates

Observed default rates varied substantially across SBA coverage categories:

Coverage	Default Rate
Low	29.49%
High	17.26%
Medium	11.33%
Very High	0.92%

The results indicate a strong historical relationship between coverage category and observed default performance.

However, this should not be interpreted as proof of causation.

5. Short-Term Loans Show Higher Observed Default Rates

The analysis found:

Loan Term	Default Rate
Short	49.07%
Medium	20.70%
Long	7.02%

Short-term loans therefore show substantially higher observed default rates in the analysed dataset.

6. High Default Rate Does Not Always Mean Highest Financial Loss

The project separates:

Default Rate → frequency of default

from

Loss Rate / Charged-Off Principal → financial impact

This distinction is important because a sector can have a high default rate while another high-volume sector may generate a larger total financial loss.

This is why the dashboard evaluates risk frequency and financial severity separately.

7. Retail Trade Has the Highest Identifiable Sector-Level Charged-Off Principal

Retail Trade recorded the highest charged-off principal among the identifiable sectors, at approximately $2.05B.

This highlights the importance of considering portfolio exposure alongside default rates.

8. Borrower Combinations Can Reveal Higher-Risk Profiles

The customer-persona analysis found that risk varies when multiple characteristics are considered together.

Examples of high-default combinations included:

Real Estate & Rental + Self-Employed — 35.65%
Finance & Insurance + Self-Employed — 34.10%
Information + Self-Employed — 31.46%
Transportation & Warehousing + 2–10 Employees — 29.80%
Construction + Self-Employed — 29.20%

This demonstrates the value of multi-dimensional borrower segmentation rather than evaluating one characteristic independently.

9. Risk Increased Sharply During the 2008 Period

The historical analysis found substantially higher observed risk during the 2008 period:

Period	Default Rate	Loss Rate
Before 2008	17.18%	6.73%
2008 period	36.01%	15.50%
After 2008	12.45%	2.91%

This demonstrates that portfolio risk should be interpreted in the context of the economic period in which loans were originated.

📌 Key Business Recommendations
1. Use Multi-Factor Risk Screening

Loan risk should not be assessed using a single variable.

Historical performance suggests considering combinations of:

Sector + Business Type + Employee Size + Loan Characteristics + SBA Coverage

2. Apply Additional Review to Higher-Risk Profiles

Borrower profiles that consistently demonstrate higher historical default rates could receive additional underwriting review rather than being automatically rejected.

3. Monitor Financial Loss Alongside Default Rate

Portfolio monitoring should combine:

Default Rate
Loss Rate
Charged-Off Principal
Loan Exposure
Loan Volume

This prevents high-volume or high-loss areas from being overlooked.

4. Monitor Geographic Concentration

States with both significant exposure and elevated historical risk should receive closer portfolio monitoring.

5. Consider Economic Context

Historical performance should be evaluated alongside the economic environment because portfolio risk can change significantly across different periods.

6. Use Historical Borrower Personas as a Screening Layer

Customer personas can help identify borrower combinations associated with higher historical risk.

However, they should support—not replace—formal credit underwriting.

🎯 Historical Risk-Screening Framework

Based on the analysis, the project proposes using historical characteristics to support a three-level risk-screening framework:

Lower Historical Risk
        ↓
Moderate Historical Risk
        ↓
Higher Historical Risk

The framework can incorporate:

Business Type
Employee Size
Sector
Loan Size
Loan Term
SBA Coverage
Historical sector/borrower performance

This is intended as a historical analytical screening framework, not a production credit-scoring model.

⚠️ Important Assumptions & Limitations
Unknown Industry

A significant number of records are classified as Unknown Industry. Attempts were made to identify the underlying sector using available fields, but the records did not consistently map to one identifiable industry.

Therefore:

Unknown Industry was retained for overall portfolio calculations.
It was excluded from selected industry-specific comparisons.
Disbursed Amount > Approved Amount

The dataset contains records where the disbursed amount exceeds the bank-approved amount.

These records were retained because removing them could introduce bias.

The available data does not establish why this occurs, so any explanation regarding additional funding remains an assumption rather than a verified fact.

Correlation Does Not Imply Causation

The analysis identifies observed relationships, not causal relationships.

For example, a higher default rate in an industry does not mean that the industry itself causes default.

Missing Credit Variables

The dataset does not contain several variables that would normally be important in real-world lending decisions, including:

Credit scores
Borrower income
Financial statements
Collateral information
Repayment history
Economic indicators
Internal lending policies

Therefore, this project should not be treated as an actual underwriting model.

Minimum Sample-Size Thresholds

Minimum loan-count thresholds were used in several comparisons to reduce the influence of small samples and potentially unstable default rates.

Historical Dataset

The findings represent historical observations in the available SBA dataset and may not directly represent current lending conditions.

📂 Project Structure
SBA-Loan-Analytics/
│
├── README.md
│
├── Data/
│   └── Cleaned SBA Dataset
│
├── SQL/
│   ├── Portfolio Analysis.sql
│   ├── Sector Analysis.sql
│   ├── Risk Analysis.sql
│   ├── Bank Analysis.sql
│   ├── Customer Persona Analysis.sql
│   └── Time Analysis.sql
│
├── Power BI/
│   └── SBA Loan Risk Dashboard.pbix
│
├── Documentation/
│   ├── Project Report.docx
│   └── SQL Business Insights.docx
│
└── Screenshots/
    ├── Portfolio Overview.png
    ├── Sector Risk Analysis.png
    ├── State Geographic Analysis.png
    └── Loan Borrower Risk Analysis.png
📊 Dashboard Preview
Portfolio Overview

Sector & Borrower Risk Analysis

State & Geographic Analysis

Loan & Borrower Risk Analysis

Replace the screenshot paths above with the exact filenames you upload to GitHub.

🚀 What This Project Demonstrates

This project demonstrates an end-to-end Data Analytics workflow:

Data cleaning and validation
Data transformation
SQL querying
Exploratory data analysis
CTEs and window functions
Risk analysis
Multi-dimensional segmentation
Customer persona analysis
KPI development
Business intelligence
Power BI dashboard development
Business interpretation
Data-driven recommendations
👤 Author

Aayush Kumbhar

Aspiring Data Analyst focused on SQL, Power BI, Excel, Python and business analytics.

⭐ Final Note

This project is an analytical case study based on historical SBA loan data. The findings and recommendations are intended to demonstrate data-driven portfolio risk analysis and should not be interpreted as an official credit assessment or lending recommendation for any financial institution.
