# NYC Bus Breakdown & Delay Analysis

## Project Overview

This project analyzes 282,192 NYC school transportation incident records containing information on bus breakdowns, delays, operators, routes, boroughs, contractor notifications, and student transportation disruptions. The objective was to investigate operational patterns contributing to transportation incidents while transforming a large, imperfect dataset into a reliable analytical resource capable of answering six business questions.

---

## Dataset Information

| Metric | Value |
| --- | --- |
| Records | 282,192 |
| Variables | 21 |
| Time Coverage | 2019–2023 |
| Incident Types | Breakdowns and Running Late |
| Tools | Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy |

---

## Business Questions

The analysis focused on the following questions:

1. What are the most common reasons for delays and breakdowns?
2. How do delay times vary by bus company and borough?
3. Is there a relationship between weekdays and transportation disruptions?
4. Are certain routes more prone to delays or breakdowns?
5. Is there a relationship between the number of students on a bus and transportation disruptions?
6. Do contractor notification practices affect transportation outcomes?

---

# Technical Workflow

## 1\. Data Understanding

Before cleaning, the dataset was profiled to assess:

- Dataset dimensions and coverage period
- Data types
- Missing\-value distribution
- Numerical distributions
- Extreme values and potential outliers
- Variable suitability for each business question

### Initial Findings

Several quality issues were identified:

- Nearly 100% missing values in Incident\_Number
- Missing values across multiple columns
- Inconsistent operator naming conventions
- Non\-standardized delay\-duration categories
- Potential anomalies in student\-count values

---

## 2\. Business Question Mapping

Before conducting analysis, each business question was mapped to the specific columns required to answer it. This ensured that data preparation activities remained aligned with the project's analytical objectives and prevented unnecessary transformations.

---

## 3\. Data Preparation

### Duplicate Validation

- Checked for duplicate observations.
- Removed duplicate records where necessary.

### Missing Value Treatment

- Assessed null counts and null percentages.
- Removed Incident\_Number due to excessive missingness.
- Imputed How\_Long\_Delayed using the modal category.
- Applied median or mode imputation to low\-missingness variables based on data type.

### Delay Duration Standardization

- Removed inconsistent text formatting.
- Standardized delay categories.
- Removed unnecessary characters and spacing.
- Produced consistent duration ranges for analysis.

### Category Standardization

- Simplified delay and breakdown reasons.
- Standardized incident classifications.
- Improved reporting and visualization consistency.

### Bus Company Name Reconciliation

- Audited all unique operator names.
- Identified naming variations for the same companies.
- Created standardized company identifiers.
- Built mapping dictionaries for reconciliation.
- Removed punctuation and formatting inconsistencies.

### Feature Engineering

- Extracted weekdays from timestamps.
- Created numerical weekday encodings.
- Generated analysis\-specific datasets for operators, boroughs, routes, notifications, and student\-count investigations.

### Iterative Data Preparation

Data preparation was not performed once at the start of the project. Additional validation, cleaning, standardization, and restructuring were performed throughout the analysis as new business questions required different analytical datasets and quality checks.

---

## 4\. Analysis and Statistical Methods

Techniques used during the project included:

- Exploratory Data Analysis (EDA)
- Frequency Analysis
- Descriptive Statistics
- Comparative Analysis
- Distribution Analysis
- Chi\-Square Test of Independence
- Cramer's V Association Analysis
- Outlier Investigation
- Data Visualization

---

## Key Findings

### Delays and Breakdowns

- Traffic was the leading cause of reported delays.
- Mechanical problems were the most common cause of breakdowns.

### Operator Performance

- Several transportation operators consistently appeared among the highest\-delay providers across multiple delay\-duration categories.

### Borough Analysis

- Manhattan, Brooklyn, and Queens experienced consistently high delay frequencies.
- The Bronx exhibited particularly high concentrations of shorter\-duration delays.

### Route Analysis

- Delay incidents were concentrated among a relatively small subset of routes.
- Breakdown incidents were more evenly distributed across routes.

### Weekday Analysis

- A statistically significant relationship between weekday and transportation disruptions was detected.
- However, Cramer's V indicated that the practical strength of this relationship was extremely weak.

### Student Count Investigation

- The student\-count variable contained substantial outliers and highly skewed values.
- Due to limited documentation and data\-quality concerns, reliable conclusions could not be drawn regarding the relationship between student counts and transportation disruptions.

### Notification Analysis

- School notifications were the most common communication practice.
- Parent notifications occurred less frequently.
- OPT notifications were reported least frequently.

---

## Challenges Encountered

- Extensive missing data.
- Inconsistent company naming conventions.
- Non\-standardized categorical values.
- Delay\-duration formatting inconsistencies.
- Student\-count outliers and questionable observations.
- Multiple rounds of cleaning required as new analytical questions emerged.

---

## Skills Demonstrated

### Data Preparation

- Data Cleaning
- Data Validation
- Missing Value Treatment
- Data Standardization
- Feature Engineering
- Data Quality Assessment

### Analysis

- Exploratory Data Analysis (EDA)
- Statistical Testing
- Pattern Discovery
- Comparative Analysis

### Visualization

- Matplotlib
- Seaborn
- Data Storytelling

### Programming

- Python
- Pandas
- NumPy
- SciPy

---

## Project Outcome

The project transformed a raw operational dataset into an analysis\-ready resource capable of answering six transportation\-focused business questions. Through extensive data preparation, exploratory analysis, statistical testing, and business interpretation, the analysis identified key drivers of delays and breakdowns while highlighting operational areas that may benefit from targeted investigation and reliability improvements.

---

**Next Step:** Open the notebook to review the complete methodology, code implementation, visualizations, statistical testing, and detailed findings.

