# EatingHabitsAndSleepQuality_dsa210-project


## The Impact of Eating Habits on Sleep Quality

### Motivation

Two of the most critical determinants of human well-being are nutrition and sleep. These two factors are closely interconnected: while poor nutrition can lead to disturbed sleep, insufficient sleep can also cause unhealthy eating behaviors. Unbalanced or unhealthy eating habits such as high sugar intake, excessive saturated fat consumption, or low fiber intake may negatively affect sleep duration, sleep latency, and sleep efficiency.

Healthy eating habits in this project are defined based on nutritional balance and food quality. Specifically, a healthy diet includes:
Appropriate caloric intake based on individual needs,
Adequate consumption of macronutrients (proteins, carbohydrates, and fats) in balanced proportions,
High intake of fruits, vegetables, and whole grains,
Limited consumption of processed foods, refined sugar, and caffeine,
Sufficient hydration and consistent meal timing throughout the day.

This project aims to analyze how these healthy eating factors influence different aspects of sleep quality using real or simulated data. The ultimate goal is to provide evidence-based insights that encourage healthier eating and better sleep outcomes.

In addition to classical statistical analysis, this project also incorporates **machine learning techniques** to examine whether sleep quality outcomes can be predicted from dietary and lifestyle variables.

---

### Objectives

Examine the relationship between overall dietary quality and sleep indicators such as total sleep duration, sleep latency, and sleep efficiency.  
Identify which nutritional components (e.g., sugar, fat, protein, calorie intake) most strongly influence sleep quality.  
Investigate the effects of meal timing (e.g., eating late at night) on sleep onset and depth.  
Explore how caffeine and hydration levels interact with diet quality to influence sleep outcomes.  
Apply machine learning models to predict sleep quality based on diet and lifestyle features.

---

### Data Sources

To conduct this project, multiple data types will be collected and analyzed to capture both dietary habits and sleep quality indicators. The data will include quantitative nutrition metrics, sleep tracking information, and relevant lifestyle variables.

#### 1. Daily Diet Logs

Data on participants’ daily food intake will be collected to assess the quality of their eating habits.

*Key variables:*
- Total daily calorie intake (kcal)
- Macronutrient ratios: percentage of protein, carbohydrates, and fat
- Micronutrient information: fiber, sugar, and saturated fat levels
- Food classification: proportion of processed vs. natural foods
- Meal timing: timestamps of main meals and snacks

#### 2. Sleep Tracking Data

Sleep-related variables will be gathered through wearable devices (e.g., Fitbit, Apple Watch) or sleep-monitoring mobile apps.

*Key variables:*
- Total sleep duration (hours)
- Sleep efficiency (% of time spent asleep while in bed)
- Deep sleep percentage (proportion of deep sleep stages)
- Sleep onset latency (minutes it takes to fall asleep)

#### 3. Self-Reported Surveys

Participants will also provide subjective assessments of their nutrition and sleep experience through questionnaires.

*Key variables:*
- Perceived sleep quality (on a 1–10 scale)
- Daily mood and stress levels
- Diet adherence and perceived healthiness

#### 4. Additional Lifestyle Variables

Since factors beyond diet can affect sleep, additional variables will be collected to control for external influences.

*Key variables:*
- Caffeine intake (cups of coffee or tea per day)
- Water consumption (liters per day)
- Physical activity level (minutes of daily exercise)
- Screen time before bed (optional variable for advanced analysis)

---

### Methodology

The project will follow a structured, data-driven analysis process:

#### Data Collection and Cleaning
- Gather nutrition and sleep data from participants or available datasets.
- Handle missing or inconsistent entries.

#### Data Categorization
- Classify individuals into healthy and unhealthy eating groups based on nutrient balance, processed food intake, and caloric ratios.
- Create binary sleep quality categories for advanced analysis.

#### Exploratory Data Analysis (EDA)
- Generate visualizations (histograms, scatter plots, correlation matrices) to explore trends between eating habits and sleep variables.

#### Statistical Analysis
- Apply correlation tests and two-sample t-tests to evaluate the significance of nutritional factors on sleep quality.

#### Machine Learning Analysis
- Formulate a supervised classification problem to predict sleep quality outcomes.
- Train baseline and ensemble machine learning models to assess predictive performance.
- Compare model outputs with statistical findings.

#### Interpretation
- Identify which eating behaviors and lifestyle factors are most predictive of good or poor sleep outcomes.
- Summarize findings in a clear, evidence-based format.

---

### Expected Outcomes

It is expected that individuals with healthier eating patterns, characterized by balanced macronutrient intake, lower sugar and processed food consumption, and consistent meal timing will show higher sleep efficiency, shorter sleep latency, and longer total sleep duration.

The analysis may also reveal that excessive caffeine, high-calorie intake before bedtime, or dehydration are linked to poorer sleep quality.

Ultimately, the results are expected to emphasize the importance of dietary balance for improved sleep and overall well-being.

---

### Limitations and Future Work

- The dataset may rely on self-reported information, which can introduce bias or inaccuracies.
- Other factors such as stress, mental health, and genetic predisposition may also influence sleep but are not directly included in this phase.
- Future work could integrate longitudinal data to observe changes in sleep patterns over time.
- Advanced machine learning models and larger datasets could improve predictive performance.
- Expanding the dataset to include different age groups or cultural dietary habits could provide more generalizable insights.

---

## Hypothesis Testing

| No. | Null Hypothesis (H₀) | Alternative (H₁) | Statistical Test & α |
|-----|----------------------|------------------|----------------------|
| 1 | There is no statistically significant relationship between healthy eating habits and sleep quality. | Healthy eating habits improve sleep quality. | Pearson correlation (α = 0.05) |
| 2 | There is no difference in sleep quality between the healthy and unhealthy diet groups. | Sleep quality differs significantly between the two diet groups. | Two-sample t-test (Healthy vs Unhealthy) |
| 3 | Sleep duration is not associated with sleep quality. | Greater sleep duration improves sleep quality. | Pearson correlation (α = 0.05) |
| 4 | Caffeine intake does not affect sleep quality. | Higher caffeine consumption lowers sleep quality. | Pearson/Spearman correlation |

> If p-value > 0.05, the null hypothesis (H₀) could not be rejected.

---

### Findings

- This project includes self-reported data of daily eating habits and sleep quality collected from **26 participants**.

- The dataset includes the following key variables:
  - Healthy Eating Score (1–10)
  - Sleep Quality Score (1–10)
  - Sleep Duration
  - Lifestyle metrics (exercise, hydration, screen time, caffeine, calories)

- The data was cleaned, categorized, and transformed into two main groups:
  - **Healthy Diet vs Unhealthy Diet**
  - **Good Sleep Quality vs Poor Sleep Quality**

- Exploratory Data Analysis (EDA) was conducted through multiple visualizations:
  - Scatter plots
  - Boxplots
  - Histograms
  - Correlation heatmaps

- Hypothesis testing was performed using Pearson correlation coefficients and two-sample t-tests.

#### Diet Category vs Sleep Quality
- **Pearson r = −0.14**, **p = 0.637**  
  → No statistically significant correlation between diet category and sleep quality.

#### Healthy vs Unhealthy Diet (t-test)
- **t-statistic = −0.48**, **p = 0.637**  
  → No statistically significant difference in average sleep score between the two groups.

---

### Machine Learning Results

- A Logistic Regression model was used as a baseline classifier due to its interpretability.
- A Random Forest classifier was implemented to capture potential non-linear relationships.
- Both models produced comparable performance, suggesting limited predictive signal in the dataset.
- Increasing model complexity did not substantially improve predictive accuracy.

---

### Interpretation

- We fail to reject the null hypotheses.
- Based on our sample (n = 26), there is **no statistically significant relationship** between diet category and sleep quality.
- Possible reasons include limited sample size, self-reported data, and unobserved lifestyle factors.

---

### Key Takeaways

- Healthier eating habits did **not** result in significantly better sleep quality in this dataset.
- Both statistical and machine learning analyses support this conclusion.
- The project highlights the importance of empirical testing over assumptions in data-driven research.

---

## Visualizations Used

### Scatter Plots
- Healthy Diet vs Sleep Quality
- Sleep Duration vs Sleep Quality
- Caffeine vs Sleep Quality

### Histograms
- Sleep Quality Distribution
- Diet Score Distribution
- Sleep Duration Distribution

### Boxplots
- Sleep Quality by Diet Category
- Sleep Duration by Diet Category

### Correlation Heatmap
- Correlation matrix of diet, sleep, hydration, and caffeine variables

---

### Use of Language Models

During the development of this project, **large language models (LLMs)** were used as a supportive tool for code debugging, refinement, and improving the clarity of documentation. All analysis design, modeling decisions, and final interpretations were made by the author.
