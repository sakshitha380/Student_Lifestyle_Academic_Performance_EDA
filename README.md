# Student Lifestyle & Academic Performance - Exploratory Data Analysis

## Project Overview

This project performs an Exploratory Data Analysis (EDA) of student lifestyle patterns and their relationship with academic performance and stress levels.

The analysis investigates how factors such as study time, sleep, social activities, extracurricular activities, and physical activity are associated with students' GPA and stress levels.

The project focuses on understanding patterns and relationships within the dataset using statistical analysis and data visualization.

> **Note:** This is an observational analysis. The relationships identified in the dataset should not be interpreted as causal relationships.

---

## Objectives

The main objectives of this project are:

- Understand the structure and quality of the student lifestyle dataset.
- Perform data cleaning and validation.
- Identify numerical, categorical, and identifier variables.
- Analyze the distribution of student lifestyle variables.
- Analyze the distribution of stress levels.
- Study relationships between lifestyle variables and GPA.
- Examine relationships between lifestyle variables and stress levels.
- Compare GPA distributions across different stress levels.
- Identify correlations among numerical variables.
- Detect potential statistical outliers.
- Summarize the major findings and insights from the dataset.

---

## Dataset

The dataset contains information about student lifestyle patterns, stress levels, and academic performance.

### Dataset Size

- Number of observations: **2,000**
- Number of columns: **8**

### Variables

| Variable | Type | Description |
|---|---|---|
| Student_ID | Identifier | Unique identifier for each student |
| Study_Hours_Per_Day | Numerical | Average study hours per day |
| Extracurricular_Hours_Per_Day | Numerical | Average extracurricular activity hours per day |
| Sleep_Hours_Per_Day | Numerical | Average sleep hours per day |
| Social_Hours_Per_Day | Numerical | Average social activity hours per day |
| Physical_Activity_Hours_Per_Day | Numerical | Average physical activity hours per day |
| GPA | Numerical | Student Grade Point Average |
| Stress_Level | Categorical | Student stress category: Low, Moderate, or High |

---

## Data Cleaning and Validation

The dataset was examined for:

- Missing values
- Duplicate records
- Invalid values
- Data types
- Identifier columns
- Numerical variables
- Categorical variables

The analysis found no missing values, duplicate records, or invalid values requiring correction.

`Student_ID` was treated as an identifier and excluded from statistical analysis.

A cleaned version of the dataset was also maintained separately.

---

## Exploratory Data Analysis

### 1. Univariate Analysis

The distributions of the numerical variables were examined using descriptive statistics, histograms, and box plots.

The variables analyzed include:

- Study Hours
- Extracurricular Hours
- Sleep Hours
- Social Hours
- Physical Activity Hours
- GPA

The stress-level distribution was also examined using category counts, percentages, and a bar chart.

---

### 2. Bivariate Analysis

The project examines three major relationships.

#### Lifestyle Variables vs GPA

Pearson correlation was used to measure the linear relationship between lifestyle variables and GPA.

The strongest relationship was observed between:

**Study Hours and GPA**

with:

**Pearson r = 0.7345**

This indicates a strong positive linear association in this dataset.

Other relationships were comparatively weak:

| Lifestyle Variable | Pearson r | Direction |
|---|---:|---|
| Study Hours | 0.7345 | Positive |
| Extracurricular Hours | -0.0322 | Negative |
| Sleep Hours | -0.0043 | Negative |
| Social Hours | -0.0857 | Negative |
| Physical Activity Hours | -0.3412 | Negative |

Study hours showed the strongest association with GPA among the lifestyle variables examined.

---

### 3. Lifestyle Variables vs Stress Level

Lifestyle variables were compared across Low, Moderate, and High stress groups.

The Kruskal-Wallis test was used because stress level consists of categorical groups and the analysis compares numerical variables across those groups.

The analysis identified statistically significant differences for several lifestyle variables across stress levels.

Important patterns included:

- Higher stress groups reported higher study hours.
- Higher stress groups showed lower sleep hours.
- Social activity differed across stress groups.
- Physical activity also differed across stress groups.
- Extracurricular activity showed little difference across stress categories.

These findings describe differences between groups and do not establish causation.

---

### 4. GPA vs Stress Level

GPA was compared across Low, Moderate, and High stress groups.

The group-level GPA results were:

| Stress Level | Count | Mean GPA | Median GPA |
|---|---:|---:|---:|
| Low | 297 | 2.8169 | 2.82 |
| Moderate | 674 | 3.0248 | 3.02 |
| High | 1029 | 3.2620 | 3.27 |

A Kruskal-Wallis test was performed to determine whether GPA distributions differed across the stress-level groups.

### Result

- H-statistic: **620.6702**
- p-value: **< 0.001**

The result indicates a statistically significant difference in GPA distributions across the three stress-level groups.

However, this statistical association should not be interpreted as evidence that stress directly causes changes in GPA.

---

## Multivariate Analysis

A Pearson correlation matrix was generated to examine relationships among the numerical variables simultaneously.

Important correlations include:

| Variable Pair | Pearson r |
|---|---:|
| Study Hours vs GPA | 0.7345 |
| Physical Activity vs GPA | -0.3412 |
| Study Hours vs Physical Activity | -0.4881 |
| Sleep Hours vs Physical Activity | -0.4703 |
| Social Hours vs Physical Activity | -0.4171 |

The correlation matrix provides an overall view of how the numerical variables are related to one another.

---

## Outlier Analysis

The Interquartile Range (IQR) method was used to identify potential outliers.

The analysis was performed on the six numerical analysis variables:

- Study Hours
- Extracurricular Hours
- Sleep Hours
- Social Hours
- Physical Activity
- GPA

`Student_ID` was excluded from outlier analysis.

Only a very small number of potential outliers were identified:

- Physical Activity Hours: **5**
- GPA: **4**

No potential outliers were identified in:

- Study Hours
- Extracurricular Hours
- Sleep Hours
- Social Hours

The identified observations were retained because they appeared to represent plausible observations rather than obvious data-entry errors.

---

## Key Findings

### Finding 1 — Study Hours and GPA

Study hours showed the strongest positive relationship with GPA.

The Pearson correlation was:

**r = 0.7345**

Students with higher reported study hours generally showed higher GPA values in this dataset.

---

### Finding 2 — Stress and Lifestyle Patterns

Different stress-level groups showed different lifestyle patterns.

Higher stress groups generally reported:

- More study hours
- Less sleep
- Different levels of social activity
- Lower physical activity

---

### Finding 3 — GPA Differs Across Stress Groups

The GPA distributions differed significantly across the three stress categories.

The mean GPA increased from:

**Low Stress → Moderate Stress → High Stress**

However, this is an observed association in the dataset and does not establish a causal relationship.

---

### Finding 4 — Weak Relationships

Extracurricular hours and sleep hours showed very weak linear relationships with GPA in the correlation analysis.

This indicates that these variables did not show a strong direct linear association with GPA in this dataset.

---

### Finding 5 — Physical Activity

Physical activity showed a moderate negative association with GPA:

**r = -0.3412**

This result should be interpreted carefully because correlation does not imply causation and other variables may influence the observed relationship.

---

## Visualizations

The project generated several important visualizations.

### Correlation Heatmap

Shows the Pearson correlations among the numerical variables.

### Lifestyle Variables vs GPA

Scatter plots show the relationship between lifestyle variables and GPA.

### Lifestyle Variables vs Stress

Visualizations compare lifestyle patterns across different stress-level categories.

### GPA Across Stress Levels

A box plot compares GPA distributions for Low, Moderate, and High stress groups.

### Stress Level Distribution

Shows the distribution of students across the three stress categories.

### Outlier Detection

Box plots are used to identify potential statistical outliers.

All important visualizations are available in:

```text
outputs/figures/