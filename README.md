# 🚌 NYC Bus Breakdown & Delay Analysis
New York City's public bus system experiences thousands of breakdowns and delays annually, disrupting commuters and straining public resources. Driven by curiosity and a passion for problem-solving, I undertook this independent project to explore key patterns, identify root causes, and generate data-driven recommendations aimed at improving service reliability.

## 📊 Project Overview

New York City's public bus system faces thousands of breakdowns and delays each year, causing frustration among commuters and resource strain for the city. As a Data Analyst, my goal was to explore patterns, uncover root causes, and suggest data-driven recommendations that could help reduce disruptions and enhance reliability.

## 🛠️ Tools & Libraries Used

- **Python**
  - `Pandas` – data cleaning, wrangling, and manipulation
  - `NumPy` – numerical operations and encoding
  - `Seaborn` & `Matplotlib` – data visualization
  - `SciPy` – statistical testing (Chi-square test)

## 🔍 Key Questions Explored

1. **What are the most common reasons for delays and breakdowns?**
2. **How do delay times vary by bus company and borough?**
3. **Is there a correlation between specific days of the week and service disruptions?**
4. **Are certain routes more prone to delays or breakdowns?**
5. **Does the number of students onboard affect delays or breakdowns?**
6. **Do contractor notifications influence how long delays last?**

## 📈 Highlights & Findings

- **Top Cause of Breakdowns:** Mechanical issues, occurring 10,399 times — **3.5× more frequently** than the next most common issue (“Won’t Start”).
- **Delay Distribution by Company:** Companies like *Leesel Transportation Corp* and *Pioneer Transportation Corp* repeatedly showed up across multiple delay-duration categories.
- **Borough-Based Delay Trends:**
  - **Bronx** had the highest count of short-term delays (0–15 min).
  - **Manhattan** reported the most medium to long delays (31–60+ min).
- **Chi-Square Test:** While the day of the week showed a statistically significant link with disruptions (p < 0.001), the effect size (Cramer's V = 0.013) was negligible — suggesting weekday isn't a strong predictor.
- **Route-Level Issues:** Certain routes (e.g., Route 2) were repeatedly flagged as high-risk for delays.

## 🧹 Data Cleaning & Processing

- Removed duplicates and high-null columns (e.g., `Incident_Number`)
- Imputed missing values using **mode** (categorical) and **median** (numerical)
- Standardized inconsistent company names using a custom mapping dictionary
- Encoded weekdays numerically and created new time-based features

## 💡 Recommendations

- **Implement mandatory service checks** every 3 months, with targeted attention to frequently reported mechanical issues.
- **Deploy route-specific strategies** for high-risk areas such as the Bronx and Manhattan.
- **Launch driver surveys** at companies with repeated long delays to identify operational inefficiencies beyond traffic.

