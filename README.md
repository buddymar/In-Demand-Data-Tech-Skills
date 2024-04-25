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

## 📌 **Data Scraping**

<p align="center">
    <kbd> <img width="1000" alt="bref" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/BRef.jpg"> </kbd> <br>
</p>

The data utilized in this analysis and predictive modeling will be sourced from a website that hosts various basketball databases, [basketball-reference.com](https://www.basketball-reference.com/). The following data will be scraped, including:
- **MVP voting results:** Distribution of votes among players who received at least one vote each season.
- **Players basic stats:** All stats typically recorded in the official box score, aggregated per game for counting stats and per year for percentage stats.
- **Players advanced stats:** Analytical stats formulated and calculated using basic stats.
- **Team stats:** Stats concerning team performance and record for each season.

All this data is scraped for the period from 2001 to present.

<br>

## 📌 **Data Integration**

In this section, all datasets will be merged into a single dataset for analysis and prediction. Before proceeding, we will conduct feature selection to eliminate columns that are unnecessary, redundant, or contain similar information to columns that will be used in the analysis.

<br>

## 📌 **Data Preprocessing**

The data cleaning section will involve various processes such as correcting errors, adjusting data types, handling missing values, managing duplicates, and so on. In the data transformation section, various processes will be performed, including adding new columns or features, handling outliers, encoding variables, correcting errors, and creating and transforming new columns.

<br>

### Data Type

All columns in this table are currently of string data type. Columns such as `Year`, `Age`, `G`, and other basketball stats should be converted to numeric format.

<br>

### Missing Values

We have identified three categories for the columns with missing values:
- `Vote_Share`: All missing values in this feature indicate that the players did not receive any MVP votes.
- **Team Stats**: Columns related to team stats have consistent missing values across them, indicating a common factor for these missing values.
- **Player Stats**: Several columns related to player stats, particularly shooting percentages, contain missing values.

<br>

### Duplicated Values

The dataset contains 0 duplicated records.

<br>

### Correcting Errors & Inconsistencies

In the dataset, there are 17 unique values for `Position` column. In basketball, especially the NBA, there are five primary positions used: PG, SG, SF, PF, and C. Therefore, there may be potential errors or inconsistencies here. 

There are quite a lot of players recorded as having multiple positions. In reality, there should be many more players recorded as having multiple positions, especially in this *position-less* era in the NBA. However, to make our data and analysis more consistent, we will use the first position recorded in the dataset.

<br>

### Creating New Columns

These are another set of columns or features created to assist in analyzing and predicting an MVP in the NBA.

Table 1 — Feature Engineering
 **New Feature** | **Explanation** |
-----------------|--------------|
MVP_rank | MVP ranking of each player for each year  
Overall_Standings | Overall standing of a team in each year
Conf_Standings | Conference standing of a team in each year
Stats_zscore | New features by transforming and standardizing all statistics within each year
prior_mvp_winner | Have you won an MVP before?
last_season_mvp | Did you win the MVP last year?
last_two_season_mvp | Did you win the last two MVPs?
total_mvp_currently | How many MVPs have you won before the current season?

<br>

## 📌 **Exploratory Data Analysis**

The Exploratory Data Analysis (EDA) will focus on analyzing all available data and information related to winning the NBA MVP award. It will primarily be divided into:
- Player Attributes
- Player Basic Stats
- Player Advanced Stats
- Teams Performance

<br>

### Player Attributes

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/vote_share.png"> </kbd> <br>
</p>

<p align="center">
    <kbd> <img width="1000" alt="pos" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/position.png"> </kbd> <br>
</p>

**Key Points:**
- MPV winners consistently receive high vote shares, often close to or exceeding 90%, indicating strong support from NBA voters for their MVP candidacy.
- Despite the subjective nature of MVP voting, the consistently high vote shares for winners suggest a certain level of consensus among voters regarding the most deserving candidate. However, there may still be biases or factors influencing the voting process, such as media coverage, team success, or individual narratives.
- While power forwards and point guards have historically dominated MVP awards from 2001 to 2023, the last three MVP winners have been centers. Centers are traditionally known for their defensive presence, rebounding, and rim protection, but recent MVP-winning centers also excel offensively, showcasing versatility in their skill sets.

<br>

### Player Basic Stats

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/basic%20stats.png"> </kbd> <br>
</p>

**Key Points:**
- MVP winners exhibit superior performance across various statistical categories compared to both MVP vote-getters and all players.
- **Statistical excellence, particularly in scoring, shooting efficiency, playmaking, and defensive contributions, appears to be a common trait among MVP winners.**

<br>

### Player Advanced Stats

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/adv%20stats.png"> </kbd> <br>
</p>

<p align="center">
    <kbd> <img width="1000" alt="pos" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/bpm.png"> </kbd> <br>
</p>

**Key Points:**
- Advanced/analytical statistics provide a more nuanced understanding of player performance, focusing on efficiency, usage, and impact on both ends of the court.
- MVP winners consistently demonstrate superior performance across various advanced metrics compared to both MVP vote-getters and all players, emphasizing their overall impact and contribution to their teams' success.
- It's undeniable that OBPM can provide more insight into a player's value than DBPM. A player can receive MVP votes solely based on their offensive performance, even if they have little defensive impact while on the court. However, it's worth noting that many MVP winners also have high DBPM, which sets them apart from other vote-getters.

<br>

### Team Stats

<p align="center">
    <kbd> <img width="1000" alt="share" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/team%20stats.png"> </kbd> <br>
</p>

<p align="center">
    <kbd> <img width="1000" alt="pos" src="https://raw.githubusercontent.com/buddymar/NBA-MVP-Predictions/main/assets/team%20win%20vs%20win%20share.png"> </kbd> <br>
</p>

**Key Points:**
- Teams with MVP-caliber players tend to outperform their counterparts in terms of offensive and defensive efficiency, margin of victory, win-loss records, and overall and conference standings.
- Higher overall and conference standings among MVP-winning teams reflect their ability to elevate team performance and competitiveness, positioning them as key leaders in guiding their teams to success within their respective conferences and the league as a whole.

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
