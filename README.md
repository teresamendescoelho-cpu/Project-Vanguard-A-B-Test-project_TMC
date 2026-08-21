# Marketing A/B Test — Campaign Effectiveness Analysis

## 📊 Project Overview

This project analyses the effectiveness of a digital advertising campaign using an **A/B testing approach**.

The objective is to determine whether showing an advertisement to users increases the likelihood that they purchase a product compared with users who were shown a public service announcement (PSA), which represents the control group.

The analysis combines **exploratory data analysis, campaign performance metrics, statistical hypothesis testing, and Tableau visualization** to provide an evidence-based business recommendation.

---

## 🎯 Business Question

**Does showing the advertisement increase the conversion rate compared with the control (PSA) group?**

The experiment contains two groups:

* **Ad group** — users exposed to the advertising campaign.
* **PSA group** — control group, where users were shown a public service announcement instead of the advertisement.

The main KPI is the **conversion rate**, representing the proportion of users who purchased the product.

---

## 🗂️ Dataset

The dataset contains one row per user and includes information about:

| Column          | Description                                    | Purpose                |
| --------------- | ---------------------------------------------- | ---------------------- |
| `user id`       | Unique identifier for each user                | Data quality checks    |
| `test group`    | Experimental group: `ad` or `psa`              | Main A/B test variable |
| `converted`     | Whether the user purchased the product         | Main outcome / KPI     |
| `total ads`     | Number of advertisements seen by the user      | Behaviour analysis     |
| `most ads day`  | Day when the user saw the most advertisements  | EDA / Tableau          |
| `most ads hour` | Hour when the user saw the most advertisements | EDA / Tableau          |

---

## 🔎 Project Workflow

The analysis follows four main stages:

### 1. Data Exploration & Cleaning

The dataset is inspected and prepared for analysis by:

* Loading the data using Pandas
* Inspecting the dataset structure
* Checking the number of rows and columns
* Reviewing data types
* Checking for missing values
* Checking for duplicated user IDs
* Reviewing unique values in the experimental and conversion variables
* Converting variables to appropriate data types where necessary
* Removing technical columns where applicable

### Exploratory Analysis

The following questions are addressed:

1. How many users are included in the dataset?
2. How many users are in the Ad group and PSA group?
3. What percentage of users converted overall?
4. What is the average number of advertisements seen per user?

### Visualizations

The exploratory analysis includes:

* Number of users by experimental group
* Conversion rate by experimental group
* Distribution of total advertisements seen per user

---

## 📈 2. Campaign Performance

The PSA group is treated as the **control group**, while the Ad group is treated as the **test/treatment group**.

The following metrics are calculated for both groups:

### Number of Users

Total number of users in each experimental group.

### Number of Conversions

Number of users for whom:

`converted = True`

### Conversion Rate

Conversion rate is calculated as:

`Conversions / Total Users`

### Conversion Rate Difference

The observed difference between the two groups is calculated as:

`Ad Conversion Rate − PSA Conversion Rate`

### Relative Improvement

The relative improvement of the Ad group compared with the PSA group is calculated as:

`(Ad Rate − PSA Rate) / PSA Rate × 100`

These metrics are used to determine whether the advertising campaign appears promising based on descriptive statistics.

---

## 🧪 3. Hypothesis Testing

The main statistical question is whether the conversion rate differs between the Ad and PSA groups.

### Null Hypothesis — H₀

> The conversion rate is the same in the Ad and PSA groups.

### Alternative Hypothesis — H₁

> The conversion rate is different between the Ad and PSA groups.

### Statistical Test

A **two-proportion z-test** is used because the analysis compares the proportions of converted users between two independent experimental groups.

The significance level is:

**α = 0.05**

The analysis reports:

* Test statistic
* P-value
* Statistical decision
* Plain-English interpretation

The decision rule is:

* If `p-value < 0.05` → reject H₀.
* If `p-value ≥ 0.05` → fail to reject H₀.

Importantly, statistical significance is considered separately from practical or business significance.

---

## 📊 4. Tableau Dashboard

A Tableau dashboard is created to communicate the main findings to a non-technical stakeholder.

### Dashboard Components

The dashboard includes:

#### KPIs

* Total users
* Conversion rate — Ad group
* Conversion rate — PSA group
* Difference between conversion rates

#### Visualizations

* Conversion rate by experimental group
* Users by experimental group
* Conversion rate by most ads day

#### Interactivity

At least one interactive filter is included using:

* Most ads day, or
* Most ads hour

The dashboard is designed to allow stakeholders to understand the campaign performance without needing to read the Python analysis.

---

## 💡 Key Findings

> **This section will be updated after the analysis is completed.**

The final analysis will report:

* Total number of users
* Number of Ad and PSA users
* Overall conversion rate
* Ad conversion rate
* PSA conversion rate
* Conversion rate difference
* Relative improvement
* Z-test statistic
* P-value
* Statistical conclusion

---

## 🏁 Final Recommendation

> **This section will be completed after the statistical analysis and Tableau dashboard are finished.**

The final recommendation will answer three key questions:

1. Did the Ad group have a higher conversion rate than the PSA group?
2. Was the observed difference statistically significant?
3. Based on the evidence, should the advertising campaign be continued?

The recommendation will distinguish between **statistical significance** and **practical/business importance**.

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas** — data manipulation and analysis
* **NumPy** — numerical calculations
* **Matplotlib** — data visualization
* **Seaborn** — exploratory visualization
* **SciPy / Statsmodels** — statistical hypothesis testing
* **Jupyter Notebook** — analysis environment
* **Tableau** — dashboard and business visualization
* **Git & GitHub** — version control and project management

---

## 📁 Project Structure

```text
Project-Vanguard-A-B-Test-project_TMC/
│
├── data/
│   └── marketing_ab_testing.csv
│
├── notebooks/
│   └── marketing_ab_test_analysis.ipynb
│
├── tableau/
│   └── marketing_ab_test_dashboard.twbx
│
├── presentation/
│   └── marketing_ab_test_presentation.pdf
│
├── README.md
└── .gitignore
```

*The exact file structure may be updated as the project develops.*

---

## 📌 Deliverables

The completed project will contain:

* 📓 **Jupyter Notebook** — complete data analysis
* 📊 **Tableau Workbook / Packaged Workbook** — final dashboard
* 📝 **README.md** — project documentation, methodology, findings and recommendation
* 🎤 **Presentation** — maximum 10-minute presentation summarizing the analysis and recommendation

---

## 📚 Skills Demonstrated

This project demonstrates practical Data Analytics skills including:

* Data cleaning
* Exploratory Data Analysis (EDA)
* Data visualization
* KPI calculation
* A/B testing
* Statistical hypothesis testing
* Interpretation of p-values
* Business-oriented data analysis
* Tableau dashboard development
* Data storytelling
* Evidence-based business recommendations

---

## 👩‍💻 Author

**Teresa Mendes Coelho**

Data Analytics Bootcamp — Ironhack

GitHub: [Teresa Mendes Coelho](https://github.com/teresamendescoelho-cpu)

---

## 📄 Project Context

This project was completed as part of the **Ironhack Data Analytics Bootcamp** and follows the provided Marketing A/B Test project brief.

The project objective is to move from:

**Raw Data → Exploration → Business Metrics → Statistical Evidence → Business Recommendation**
