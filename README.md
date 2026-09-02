# Kaggle Data Science & Machine Learning Survey Analysis (2017–2021)

A complete exploratory analysis of Kaggle's annual Data Science & Machine Learning Survey, covering **106,301 responses across 293 questions** from five consecutive survey years (2017–2021). This project explores respondent demographics, career background, and the tools, languages, and frameworks the data science community actually uses.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Key Findings](#key-findings)
- [Who Took the Survey](#who-took-the-survey)
- [Career Background](#career-background)
- [Tools of the Trade](#tools-of-the-trade)
- [Machine Learning & BI Tools](#machine-learning--bi-tools)
- [Conclusion](#conclusion)
- [Repository Structure](#repository-structure)
- [How to Run](#how-to-run)

## Overview

Every year, Kaggle surveys people working in and around data science about who they are, what they know, and what tools they use. This project combines five years of that survey (2017–2021) into a single analysis to track how the community and its tooling have changed over time.

The full workflow, cleaning, aggregation, and every chart, lives in [`notebook/kaggle-survey-analysis-2017-2021.ipynb`](notebook/kaggle-survey-analysis-2017-2021.ipynb). A stakeholder-friendly write-up is also included as a Word document in [`report/`](report/).

## Dataset

- **Source:** [Kaggle Data Science and ML Survey, 2017–2021](https://www.kaggle.com/datasets/andradaolteanu/kaggle-data-science-survey-20172021) (combined by Andrada Olteanu)
- **Size:** 106,301 rows × 293 columns
- **Years covered:** 2017, 2018, 2019, 2020, 2021
- **Note:** Programming language, IDE, and ML framework questions were not asked in 2017, so those sections cover 2018–2021 only.

Cleaning steps applied before analysis:
- Fixed encoding issues in text fields (e.g. `Bachelorâ€™s degree` → `Bachelor's degree`)
- Standardized inconsistent category labels across years (e.g. `"1 to 2 years"` vs `"1-2 years"`)
- Merged overlapping country names, job titles, and tool names into consistent categories

## Key Findings

- **Python dominates.** Python usage grew from ~15,700 mentions in 2018 to ~21,900 in 2021 (+39%), pulling further ahead of every other language.
- **Scikit-Learn leads ML frameworks** with ~45,900 total mentions (2018–2021), but **PyTorch is the fastest growing**, up ~60% over the same period.
- **Visual Studio overtook Jupyter** as the most-used development environment in 2021, after Jupyter led every prior year.
- **Tableau and Microsoft Power BI** together account for roughly two-thirds of all BI tool mentions.
- **The gender gap remains wide**, with ~80% of respondents identifying as male in every survey year.
- **Students are the single largest respondent group** (~24%), which should be kept in mind when interpreting experience and tool-usage figures.

## Who Took the Survey

Response volume grew across the five years, from around 16,700 in 2017 to roughly 26,000 in 2021.

![Responses by Year](images/01_responses_by_year.png)

### Age

Respondents skew young: the 25–29 age group is the largest single band (~22%), and well over half of all respondents are under 35.

![Age Distribution](images/02_age_distribution.png)
![Age by Year](images/03_age_by_year.png)

### Gender

About 4 in 5 respondents identify as male and roughly 1 in 5 as female, a split that has stayed fairly constant across all five years.

![Gender Distribution](images/04_gender_distribution.png)
![Gender by Year](images/05_gender_by_year.png)

### Country

India and the United States lead by a wide margin, followed by Brazil, China, Russia, and the United Kingdom.

![Top 10 Countries](images/06_country_top10.png)
![Country by Year](images/07_country_by_year.png)

### Education

This is a highly educated community: about 43% hold a master's degree and 34% a bachelor's degree, with close to 9 in 10 respondents holding a four-year degree or higher.

![Education Level](images/08_education_level.png)
![Education by Year](images/09_education_by_year.png)

## Career Background

### Current Role

Students make up the largest group of respondents (~24%), followed by Data Scientist (~19%), Software Engineer, Data Analyst, and Research Scientist.

![Top 10 Roles](images/10_top_roles.png)
![Roles by Year](images/11_roles_by_year.png)

### Coding Experience

Roughly half of all respondents report two years of coding experience or less, reflecting the large student and early-career population.

![Coding Experience](images/12_coding_experience.png)
![Experience by Year](images/13_experience_by_year.png)

## Tools of the Trade

### Programming Languages

Python leads by a wide margin (~65,900 mentions, 2018–2021), followed by SQL (~33,100) and R (~20,900). R usage actually declined slightly over the period while Python and SQL both grew.

![Languages Overall](images/14_languages_overall.png)
![Languages Trend](images/15_languages_trend.png)

### Development Environments

Jupyter led every year through 2020, but Visual Studio surged in 2021 to become the most-used environment, overtaking Jupyter for the first time.

![IDE Usage Overall](images/16_ide_overall.png)
![Most Used IDEs](images/18_ide_most_used.png)
![IDE Trend](images/17_ide_trend.png)

## Machine Learning & BI Tools

### ML Frameworks

Scikit-Learn is the clear leader overall, but PyTorch shows the strongest year-over-year growth, closing the gap with TensorFlow and Keras.

![ML Frameworks Overall](images/19_ml_framework_overall.png)
![ML Frameworks by Year](images/20_ml_framework_by_year_1.png)
![ML Frameworks by Year (Percent)](images/21_ml_framework_by_year_2.png)

### Business Intelligence Tools

Tableau and Microsoft Power BI dominate the BI space, together accounting for roughly two-thirds of all mentions.

![BI Tools](images/23_bi_tools.png)

## Conclusion

Despite the constant hype around deep learning, traditional machine learning tools, led by Scikit-Learn, remain the everyday standard, likely because they require less infrastructure and are easier to learn than deep learning pipelines. Python has cemented itself as the default language of the field, and the shift toward Visual Studio as a development environment shows that tool preferences are still evolving.

One caveat: students make up a large share of respondents, and their tool choices and experience levels can differ from working professionals, which may pull some results (like coding experience and tool familiarity) toward what a learner would choose. Even so, the overall pattern is clear: data science is a fast-growing, global, increasingly standardized field, with Python, Scikit-Learn, and Jupyter-style notebooks at its core.


```

## How to Run

```bash
git clone https://github.com/<your-username>/kaggle-survey-analysis-2017-2021.git
cd kaggle-survey-analysis-2017-2021
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook notebook/kaggle-survey-analysis-2017-2021.ipynb
```

You'll need the source CSV (`kaggle_survey_2017_2021.csv`) from the [Kaggle dataset page](https://www.kaggle.com/datasets/andradaolteanu/kaggle-data-science-survey-20172021) placed in the path referenced at the top of the notebook.


