## Assignment 3: Apply CRISP-DM process for European Soccer Football dataset

Note! There is a lot of "artistic freedom" in this assignment, so don't think only about the points and try to come up with something new and creative from the data.

Note! A concise and focused answer is better than a long and broad one also to this assignment.

### Add your information 

**TODO**: Add your name or names: 
* student_name = 'student name/names'
* student_email = 'student email/emails'

Assignments for the first two phases of the CRISP-DM model based on football:

This is a free-form task for which there is no so-called correct answer.

## Background information about the data

The dataset used in this assignment is the [European Soccer Database](https://www.kaggle.com/datasets/hugomathien/soccer/data) from Kaggle.com. The database has been created using web crawling scripts from the following websites:
1. http://football-data.mx-api.enetscores.com/: results, lineups, team information and events
2. http://www.football-data.co.uk/: betting odds
3. http://sofifa.com/: player and team attributes from EA Sports FIFA games

In this assignment you must load dataset yourself from the Kaggle.

The data in the database includes:
* +25000 matches
* +10000 players
* 11 European football leagues
* From the seasons 2008-2016
* The source of the player and team attributes has been the sofifa website of the "EA Sports FIFA" video games.
* Match lineups with positions
* Betting odds from 10 different betting service providers
* Match metadata, i.e. match scorecard entries (goal types, possession, corners, cards, etc.) for over 10,000 matches.


## 3.1. Business Understanding (3 points)

The goal is to understand what problem the analysis is trying to solve and what the business benefit is.

**Questions**:

* Define the main goal of the analysis: Do you want to predict match results, analyze player performance, study betting profitability, focus on just one football league or something else?
* Identify stakeholders: Who benefit from the analysis (coaches, players, bettors, clubs, spectators, fans)?
* What kind of analyses do different stakeholders want from the data?
* Define target metrics: E.g. accuracy of win predictions, measuring player efficiency in certain areas.
* List the most important variables: E.g. goals, assists, player attributes, betting odds.
* Define the target group or groups for the next phase (coaches, players, bettors, clubs, spectators, fans). It is not advisable to choose a target group that is too broad.
* Consider whether the data needs to be supplemented for future analysis.

Business Understanding can be written in either a Markdown file or a Jupyter Notebook file.

The base file for the assignment can be found at [assignment_3_1_business_understanding.md](./assignment_3_1_business_understanding.md) file.

## 3.2. Data Understanding (7 points)

This phase of the project examines the data and its quality. Implement the assignment 3.2 as a **Jupyter Notebook** file.

Use the draft implementation [Football database reader](database_structure/assignment_3_2_data_understanding_draft.ipynb) 
as a guide by downloading the dataset from Kaggle and doing your own initial data analysis to understand the dataset being used.

Define the target group or groups for the next phase (coaches, players, bettors, clubs, spectators, fans).
You can choose the perspective, and it will certainly have a significant impact on the analysis. Therefore, the questions below are examples, but
the implementation depends on whom the analysis is aimed at.

**Questions**:

1. Dataset structure: What are the main tables and the connections between them?
2. Missing values: Are there gaps in player attributes or match data?
3. Outliers and errors: Are there, for example, unrealistic player heights or incorrect match results?
4. Distribution of variables: Is, for example, the goal average realistic and reasonable?
5. Visualization: For example, team goal averages, point averages, player age distribution or betting odds dispersion.
6. Modeling: planning of possible machine learning models based on dataset.

This phase ensures that the analysis is based on business-useful and high-quality data.

Clarifying questions for the Data Understanding phase

### 3.2.1. Dataset structure

* How many rows and columns are there in each SQL table?
* What is the time period for which the data is available?
* Is the data continuous or are there gaps in the time series?
* How comprehensive is the data from different leagues and teams?
* Are there any differences in data coverage at the league level?
* See basic info and statistics of dataset

### 3.2.2. Missing values 

* Are there missing (NaN) values in the dataset, and how should they be handled?
* Should NaN values be deleted rather than replaced?

### 3.2.3. Outliers and errors

* Are some variables always zero or the same values, which may indicate a data quality problem?
* Are there any outliers in matches or players (e.g. a player scoring 1000 goals in a season)?
* Are there unrealistic values in the players' characteristics? (e.g. players height is 250 cm)

### 3.2.4. Distribution of variables

* Can the distribution of variables be used to identify errors in the data?
* Are the players' characteristics normally distributed? (e.g. players' weights or heights may follow a normal distribution.)
* Are there many zeros in the distribution or is one value overemphasized? (e.g. Sometimes -1 is used as a substitute value in datasets)
* Are there illogical relationships between variables in the data (e.g. a team has 3 shots in a game, but 5 goals)
* How can you visualize the distribution of variables in the data?

### 3.2.5. Visualization

* How are goals scored on average in different leagues? Distinguish between home and away games.
* Which teams score the most and the fewest goals per match?
* Has the average goal or point average changed over time? (i.e. time series visualization is needed)
* How do the betting odds of different companies correlate with the actual results of the matches?

### 3.2.6. Modeling

* What kind of machine learning models could you build based on this data?
* Again, consider the stakeholder, i.e. who the modeling is being done for
* Note! This is only planning task in this assignment. No real modeling is needed to do with the dataset.
