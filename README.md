# 📊 In-Demand Data Tech Skills: A Closer Look
<br>

**Platform**: Jupyter Notebook | [Notebook via nbviewer](https://nbviewer.org/github/buddymar/In-Demand-Data-Tech-Skills/blob/main/In%20Demand%20Data%20Tech%20Skills.ipynb) | [Notebook via Github](https://github.com/buddymar/In-Demand-Data-Tech-Skills/blob/main/In%20Demand%20Data%20Tech%20Skills.ipynb)<br>
**Programming Language**: Python <br>
**Libraries**: Pandas, NumPy, Matplotlib, Seaborn <br>
**Source Data**: IBM Data Analyst Certification Capstone Project via Coursera | [Stack Overflow](https://stackoverflow.blog/2019/04/09/the-2019-stack-overflow-developer-survey-results-are-in/) <br>
<br>

**Table of Contents**
- [Introduction](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#-introduction)
- [Data Source](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#-data-scraping)
- [Data Preprocessing](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#-data-preprocessing)
	- [Data Cleaning](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#-data-preprocessing)
      - [Missing Values](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Duplicated Values](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#duplicated-values)
- [Exploratory Data Analysis](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#-exploratory-data-analysis)
  - [Tech Skills Dataset](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#player-attributes)
      - [Programming Language](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Database](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Platform](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Web Frame](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [IDE](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
  - [Demographic Dataset](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#player-basic-stats)
      - [Respondent Description](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Age](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Gender](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Country](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Formal Education Level](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Undergrad Major / Field of Study](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Non-degree Education](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Developer Type / Job Title](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Annual Salary](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
  - [Data Analyst](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#player-advanced-stats)
      - [Tech Skills - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Formal Education Level - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Undergrad Major / Field of Study - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Non-degree Education - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Annual Salary - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Annual Salary Comparison For Total Skill(s) Used - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
      - [Annual Salary Comparison For Each Tech Skills - DA](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#missing-values)
- [Conclusion](https://github.com/buddymar/NBA-MVP-Predictions/blob/main/README.md#-predictive-modeling)

<br>

---

## 📌 **Introduction**

<p align="center">
    <kbd> <img width="1000" alt="mvp banner" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/data%20skills%20banner.jpg"> </kbd> <br>
</p>

In today's rapidly evolving digital landscape, the demand for professionals equipped with data-related skills is soaring. From data analysts to data scientists, individuals proficient in harnessing the power of data are becoming indispensable assets across industries. In this analysis, we delve into the intricacies of in-demand data tech skills, exploring the key competencies, trends, and insights shaping the data-driven ecosystem.

Through a meticulous analysis of industry demands, job market trends, and emerging technologies, we aim to provide a comprehensive overview of the data tech landscape. By examining the core skills sought after by employers, understanding the nuances of different roles, and highlighting the latest advancements in data technologies, we offer valuable insights for aspiring professionals and seasoned practitioners alike.

<br>

## 📌 **Data Source**

Stack Overflow, a popular website for developers, conducted an online survey of software professionals across the world. The survey data was later open sourced by Stack Overflow. The actual data set has around 90,000 responses. The dataset used in this notebook comes from the following [source](https://stackoverflow.blog/2019/04/09/the-2019-stack-overflow-developer-survey-results-are-in/) under a ODbL: Open Database License. **Note:** this randomised subset contains around 1/10th of the original data set.

[This file](https://github.com/kudou88/In-Demand-Data-Tech-Skills/blob/52e1577eb7957a937c3b6c0c7223cdd450b50653/about_dataset.pdf) list the questions asked in the survey and a general description of each questions.

There are two CSV files from this Stack Overflow survey.
- The first file *`m5_survey_data_technologies_normalised.csv`* contains a list of programming skills that are currently being used and would like to be work in over next five years (by each respondent). 
- The second file *`m5_survey_data_demographics.csv`* contains demographic information for each respondent who filled out this survey.

<br>

## 📌 **Data Preprocessing**

The data cleaning section will involve various processes such as correcting errors, adjusting data types, handling missing values, managing duplicates, and so on.

<br>

### Missing Values

Based on the quick overview of the datasets, there are numerous missing values present. However, during the survey, respondents were permitted to provide no answer or skip questions. Therefore, all missing values in this dataset (*except in cases where an entire respondent/record/feature consists of missing values*) will not be handled and will be used as they are.

<br>

### Duplicated Values

The dataset contains 0 duplicated records.

<br>

## 📌 **Exploratory Data Analysis**

### </> Tech Skills Dataset

<br>

### Programming Language

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_lang1.png"> </kbd>
</p>

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_lang2.png"> </kbd>
</p>

**Among the top 5 programming languages currently in use or sought after, `TypeScript` demonstrates the most significant growth at 26.49%, while `Bash/Shell/PowerShell` experiences the most notable decline at -33.28%.**

<br>

### Database

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_db1.png"> </kbd>
</p>

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_db2.png"> </kbd>
</p>

**Among the top 5 databases presently in use or sought after, 'Elasticsearch' exhibits the most substantial growth at 46.16%, whereas 'MySQL' experiences the most considerable decline at -40.01%.**

<br>

### Platform

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_platform1.png"> </kbd>
</p>

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_platform2.png"> </kbd>
</p>

**Among the top 5 platforms currently utilized or aspired to, `Docker` demonstrates the most significant growth at 32.57%, whereas `Windows` experiences the most notable decline at -30.11%.**

<br>

### Web Frame

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_webframe1.png"> </kbd>
</p>

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_webframe2.png"> </kbd>
</p>

**Among the top 5 web frameworks currently utilized or sought after, `Vue.js` exhibits the most substantial growth at 111.65%, whereas `jQuery` experiences the most significant decline at -51.59%.**

<br>

### IDE

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/a_ide.png"> </kbd>
</p>

<br>

### 👥 Demographic Dataset

<br>

### Respondent Description

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_desc.png"> </kbd>
</p>

The majority of respondents who took this survey described themselves as a developer as a profession.

<br>

### Age

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_age.png"> </kbd>
</p>

The majority of respondents who took part in this survey were in the range of 25-35 years.

<br>

### Gender

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_gender.png"> </kbd>
</p>

In the developer profession, the male gender still dominates compared to other genders.

<br>

### Country

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_country.png"> </kbd>
</p>

The graph above contains the 20 countries with the highest number of respondents in this survey. Most respondents came from the United States. Furthermore, most of the other respondents came from India, UK, Germany, and Canada.

<br>

### Formal Education Level

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_edu.png"> </kbd>
</p>

The majority of the last education level of the respondents in this survey is Bachelor Degree. After that there is a Master Degree and some college/university study (without degree).

<br>

### Undergrad Major / Field of Study

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_major.png"> </kbd>
</p>

The majority of the majors taken by respondents who work as developers are **computer science, computer engineering, or software engineering**. Other majors taken by the developers in this survey are **information systems, information technology, or system administration**; **another engineering discipline (ex. civil, electrical, mechanical);** and **web development or web design**. Almost all majors taken by respondents with the developer profession are majors in the IT field.

<br>

### Non-degree Education

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_nondeg.png"> </kbd>
</p>

In addition to formal education, various activities/other education (non-degree) can also be used to gain knowledge, experience, and even get a profession as a developer. The non-formal activities/education most used by respondents are **self-taught, online courses, and on-the-job training.**

<br>

### Developer Type / Job Title

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_devtype.png"> </kbd>
</p>

The majority of respondents in this survey have positions as full-stack developer, back-end developer, front-end developer, desktop developer, and mobile developer. **Of all respondents, there are 802 people who work as data/business analysts.**

<br>

### Salary

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/In-Demand-Data-Tech-Skills/main/assets/b_salary.png"> </kbd>
</p>

The annual salary distribution of the survey respondents is in the form of a right-skewed distribution. The majority of annual salaries are in the range of $27,000-$100,000. The largest annual salary in this dataset is $2,000,000.

<br>

<br>

## 📌 **Predictive Modeling**

To predict the NBA MVP from this dataset, three models will be compared: Random Forest, XGBoost, and Extra Trees Regressor. The best-performing model will then be used for predicting and tracking the current season's NBA MVP. Given the imbalanced nature of the target variable, which often includes many zero values, the Root Mean Squared Logarithmic Error (RMSLE) will be used as the scoring metric.

<br>

### Modeling

Table 2 — Model Scoring
 **Model** | **RMSLE** | **R-squared** | **Best Hyperparameters** |
-----------------|--------------|--------------|--------------|
RandomForestRegressor | 0.2333 | 0.9063 | 'max_depth': 8, 'max_features': 'auto', 'min_samples_leaf': 3, 'min_samples_split': 6, 'n_estimators': 100
ExtraTreesRegressor | 0.2408 | 0.9087 | 'max_depth': 7, 'max_features': 'auto', 'min_samples_leaf': 3, 'min_samples_split': 6, 'n_estimators': 100
XGBRegressor | 0.155 | 0.9705 | 'colsample_bytree': 1.0, 'gamma': 0.1, 'learning_rate': 0.05, 'max_depth': 6, 'min_child_weight': 3, 'n_estimators': 63, 'reg_alpha': 0.5, 'reg_lambda': 1.0, 'subsample': 0.9
<br>

### Model Prediction

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/model%20prediction.png"> </kbd> <br>
</p>

**Key Points:**
- Based on the NBA MVP predictions for 2001-2023 winners, the XGBoost model had the best performance, achieving the highest accuracy with 22 correct predictions out of 23 winners. The Extra Trees model made 19 correct predictions, while the Random Forest model made 18 correct predictions.
- Interestingly, all three models incorrectly predicted the MVP for the 2017 season, selecting James Harden instead of Russell Westbrook.
- Moreover, all three models predict Nikola Jokić as the MVP for the current 2024 season (as of March), with a high predicted vote share.
- Overall, the models demonstrated high accuracy in predicting the NBA MVP, with XGBoost leading the pack with an accuracy ratio of 22 out of 23 (95.65%).

<br>

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/top3%20mvp.png"> </kbd> <br>
</p>

**Key Points (as of March 2024):**
- Nikola Jokić, with the highest PER, WS, and BPM, likely contributes significantly to the model predicting him as the number one of the top 10 MVP frontrunners.
- Shai Gilgeous-Alexander (2nd) and Giannis Antetokounmpo (3rd) still have a chance to move up in the MVP ranking ladder based on their actual basic stats, advanced stats, team standings, and vote share prediction.
- Luka Dončić leads in PTS per game (34.1) this season, with a considerable gap to the second highest, Shai Gilgeous-Alexander (30.9). This contributes to Dončić being in 4th place currently, despite his team's poor standings.

<br>

### Model Interpretation

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/shap%20value.png"> </kbd> <br>
</p>

The feature with the highest impact on the XGBoost model prediction is `adj_W%`, which represents the team's winning percentage adjusted by the total basic stats of the player. The impact gap from this feature to the next feature is considerable. Following closely are the next two impactful features for the model: `Total_AdvStat`, representing the total advanced stats for the player, and adjusted `BPM`, which indicates the Box Plus/Minus of the player.

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/shap%20bee.png"> </kbd> <br>
</p>

From the beeswarm plot, we can discern in greater detail the influence of each feature in this model. The plot vividly illustrates the wide range of impact from the `adj_W` feature. Additionally, it's apparent that features with high-value records exert the most influence on the model's predictions. Conversely, most low-value records result in zero impact across all features, except for `AST`, `Age`, and `Year`.

<br>

## 📌 **Dashboard**

Utilizing the same dataset analyzed earlier, this dashboard offers an additional perspective on NBA player performance and facilitates comparisons between player statistics. The dashboard consists of two sections: Leaderboard and Player Detailed Stats.

In the Leaderboard section, users can view the top 10 leaders in various statistics for each year or team. Meanwhile, the Player Stats section provides detailed information on selected player statistics, including the actual values, percentiles against other players each year, and comparisons to other players.

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/dash1.png"> </kbd> <br>
</p>

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/dash2.png"> </kbd> <br>
</p>
