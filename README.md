# Marketing A/B Test — Campaign Effectiveness Analysis

## 📊 Project Overview

This project analyses the effectiveness of a digital advertising campaign using an **A/B testing approach**.

The objective is to determine whether showing an advertisement to users increases the likelihood that they purchase a product compared with users who were shown a public service announcement (PSA), which represents the control group.

The analysis combines **exploratory data analysis, campaign performance metrics, statistical hypothesis testing, and Tableau visualization** to provide an evidence-based business recommendation.

---

## 🎯 Business Question

**Does showing the advertisement increase the conversion rate compared with the control (PSA) group?**

The experiment contains two groups:

- **Ad group** — users exposed to the advertising campaign.
- **PSA group** — control group, where users were shown a public service announcement instead of the advertisement.

The main KPI is the **conversion rate**, representing the proportion of users who purchased the product.

---

## 🗂️ Dataset

The dataset contains one row per user and includes:

| Column | Description | Purpose |
|---|---|---|
| `user id` | Unique identifier for each user | Data quality checks |
| `test group` | Experimental group: `ad` or `psa` | Main A/B test variable |
| `converted` | Whether the user purchased the product | Main outcome / KPI |
| `total ads` | Number of advertisements seen by the user | Behaviour analysis |
| `most ads day` | Day when the user saw the most advertisements | EDA / Tableau |
| `most ads hour` | Hour when the user saw the most advertisements | EDA / Tableau |

---

# 🔎 Project Workflow

The analysis follows four main stages:

## 1. Data Exploration & Cleaning

The dataset was inspected and prepared for analysis by:

- Loading the data using Pandas
- Inspecting the dataset structure
- Checking the number of rows and columns
- Reviewing data types
- Checking for missing values
- Checking for duplicated user IDs
- Reviewing unique values in the experimental and conversion variables
- Converting variables to appropriate data types where necessary
- Removing technical columns where applicable

### Exploratory Analysis

The analysis addresses:

1. How many users are included in the dataset?
2. How many users are in the Ad group and PSA group?
3. What percentage of users converted overall?
4. What is the average number of advertisements seen per user?

### Visualizations

- Number of users by experimental group
- Conversion rate by experimental group
- Distribution of total advertisements seen per user

---

# 📈 2. Campaign Performance

The PSA group is treated as the **control group**, while the Ad group is treated as the **test/treatment group**.

### Conversion Rate

`Conversions / Total Users`

### Conversion Rate Difference

`Ad Conversion Rate − PSA Conversion Rate`

### Relative Improvement

`(Ad Rate − PSA Rate) / PSA Rate × 100`

---

# 🧪 3. Hypothesis Testing

The main statistical question is whether the conversion rate differs between the Ad and PSA groups.

### Null Hypothesis — H₀

> The conversion rate is the same in the Ad and PSA groups.

### Alternative Hypothesis — H₁

> The conversion rate is different between the Ad and PSA groups.

A **two-proportion z-test** was used to compare the proportions of converted users between the two independent experimental groups.

**Significance level: α = 0.05**

Decision rule:

- If `p-value < 0.05` → reject H₀.
- If `p-value ≥ 0.05` → fail to reject H₀.

Statistical significance is considered separately from practical or business significance.

---

# 📊 4. Results

## Campaign Performance

| Metric | Ad | PSA |
|---|---:|---:|
| Users | **564,577** | **23,524** |
| Conversions | **14,423** | **420** |
| Conversion Rate | **2.5547%** | **1.7854%** |

### Conversion Rate Difference

**+0.7692 percentage points** (approximately **+0.77 p.p.**)

### Relative Improvement

**+43.09%** relative improvement for the Ad group compared with the PSA control group.

## Statistical Test Results

| Statistic | Result |
|---|---:|
| Z-statistic | **7.3701** |
| P-value | **1.7053 × 10⁻¹³** |
| Significance level | **0.05** |
| Decision | **Reject H₀** |

Since the p-value is substantially below 0.05, there is **statistically significant evidence that the conversion rates differ between the Ad and PSA groups**.

---

# 📊 5. Tableau Dashboards

## Dashboard 1 — Marketing A/B Test Performance Dashboard

The main dashboard provides an executive overview of the experiment.

### KPIs

- Total Users
- Ad Conversion Rate
- PSA Conversion Rate
- Conversion Rate Difference

### Visualizations

- Conversion Rate by Experimental Group
- Users by Experimental Group
- Conversion Rate by Most Ads Day

---

## Dashboard 2 — Advertising Performance by Hour

A second dashboard analyses campaign performance throughout the day.

It includes:

- Total Ads by Hour
- Conversion Rate by Hour
- Conversion Rate Difference by Hour
- Relative Improvement by Hour

This dashboard provides additional behavioural insight into how advertising exposure and conversion performance vary across different hours.

---

## Dashboard 3 — A/B Test Group Performance

This dashboard focuses specifically on the comparison between the **Ad** and **PSA** experimental groups.

### Visualizations

- Conversion Rate by Group
- Conversion Rate Difference by Group
- Relative Improvement
- Total Ads by Group

The dashboard makes the treatment-versus-control comparison clear and highlights the performance advantage of the Ad group.

---


# 💡 Key Findings

1. **The Ad group had a higher conversion rate:** 2.55% versus 1.79% for PSA.
2. **The absolute improvement was 0.77 percentage points.**
3. **The relative improvement was 43.09%.**
4. **The difference was statistically significant:** Z = 7.3701 and p = 1.7053 × 10⁻¹³.
5. **The hourly analysis shows that campaign performance varies considerably across the day, providing opportunities for further optimisation.**


---

# 🏁 Final Recommendation

Based on the A/B test results, **the advertising campaign should be continued**.

The Ad group achieved a higher conversion rate than the PSA control group, with **2.55% versus 1.79%**. This represents a **0.77 percentage-point increase** and a **43.09% relative improvement**.

The observed difference was statistically significant, with a p-value substantially below the 0.05 significance threshold.

However, statistical significance should be distinguished from practical business impact. The company should continue monitoring campaign performance and compare the additional conversions generated with the **cost of advertising** to determine whether the campaign delivers sufficient return on investment.

---

# 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SciPy / Statsmodels**
- **Jupyter Notebook**
- **Tableau**
- **Git & GitHub**

---

# 📁 Project Structure

```text
Project-Vanguard-A-B-Test-project_TMC/
│
├── data/
│   ├── marketing_AB.csv
│   └── marketing_AB_clean.csv
│
├── notebooks/
│   └── Marketing_AB_Test_Analysis.ipynb
│
├── .gitignore
├── Tableau workbook / packaged workbook
└── README.md
```

---

# 📌 Deliverables

- 📓 **Jupyter Notebook** — complete data analysis
- 📊 **Tableau Workbook / Packaged Workbook** — dashboards and visual analysis
- 📝 **README.md** — project documentation
- 🎤 **Presentation** — maximum 10-minute presentation summarizing the analysis and recommendation

---

# 📚 Skills Demonstrated

- Data cleaning
- Exploratory Data Analysis (EDA)
- Data visualization
- KPI calculation
- A/B testing
- Statistical hypothesis testing
- Interpretation of p-values
- Business-oriented data analysis
- Tableau dashboard development
- Data storytelling
- Evidence-based business recommendations

---

# 👩‍💻 Author

**Teresa Mendes Coelho**

Data Analytics Bootcamp — Ironhack

GitHub: [Teresa Mendes Coelho](https://github.com/teresamendescoelho-cpu)

---

## 📄 Project Context

This project was completed as part of the **Ironhack Data Analytics Bootcamp** and follows the Marketing A/B Test project brief.

The project objective is to move from:

**Raw Data → Exploration → Business Metrics → Statistical Evidence → Business Recommendation**
