# Amazon-Prime-EDA
Exploratory Data Analysis of Amazon Prime Movies and TV Shows using Python
## Project Overview

This project performs Exploratory Data Analysis (EDA) on an Amazon Prime Video dataset containing Movies and TV Shows.

The objective is to understand the characteristics of the Amazon Prime content library by analyzing content type, genres, release trends, runtime, IMDb ratings, audience votes, TMDB popularity, age certification, and other relevant attributes.

---

## Problem Statement

Amazon Prime Video offers a large library of movies and TV shows across multiple genres, languages, and countries. Understanding the characteristics of this content library can help identify meaningful patterns and trends.

This project aims to analyze the Amazon Prime Video dataset and answer important business questions related to:

- Distribution of Movies and TV Shows
- Common genres
- Content release trends
- Runtime patterns
- IMDb ratings
- IMDb votes
- TMDB popularity
- Age certification
- Relationships between runtime, ratings, and popularity

---

## Business Objective

The objective of this project is to perform Exploratory Data Analysis on the Amazon Prime Video dataset to identify meaningful patterns and trends in the available content.

The analysis focuses on understanding:

- Content distribution
- Genre patterns
- Release trends
- Runtime differences
- Audience ratings
- Regional content characteristics
- Relationships between different content performance metrics

---

## Dataset

The project uses two datasets:

### 1. titles.csv

The titles dataset contains information such as:

- Title
- Content type
- Description
- Release year
- Age certification
- Runtime
- Genres
- Production countries
- Seasons
- IMDb score
- IMDb votes
- TMDB popularity
- TMDB score

### 2. credits.csv

The credits dataset contains information related to the cast and crew associated with the titles.

After cleaning and removing duplicate title records, the final EDA dataset contains **9,868 unique titles**.

---

## Hypotheses and Assumptions

### Hypotheses

1. Movies are expected to have a longer average runtime than TV Shows.
2. Movies and TV Shows may have different average IMDb ratings.
3. Some genres may have higher average IMDb ratings than others.
4. Newer content may have different average IMDb ratings compared with older content.
5. Titles with higher IMDb ratings may tend to receive a higher number of IMDb votes.
6. Runtime may have a relationship with IMDb ratings.
7. More popular titles may also have higher IMDb ratings.

### Assumptions

- The available datasets are assumed to represent the Amazon Prime Video content contained in the source dataset.
- Missing categorical information such as age certification is represented as `Unknown` where required for analysis.
- IMDb score and IMDb votes are treated as indicators of audience response in this analysis.
- The analysis is based on the available records in the dataset and may not represent the complete or current Amazon Prime Video catalog.

---

## Data Preparation

The following steps were performed during data preparation:

- Loaded the `titles.csv` and `credits.csv` datasets.
- Inspected the structure and data types of the datasets.
- Checked for missing values.
- Identified and removed duplicate records.
- Merged the titles and credits datasets.
- Removed duplicate title entries after merging.
- Prepared the final EDA dataset for analysis.
- Converted list-like genre information into usable lists for analysis.

---

## Feature Engineering

The following features were created:

- **Release Decade** - Groups release years into decades.
- **Runtime Category** - Categorizes runtime into Short, Medium, and Long.
- **Content Age** - Represents the age of content based on its release year.
- **Number of Genres** - Counts the genres associated with each title.
- **Number of Production Countries** - Counts the production countries associated with each title.

---

## Exploratory Data Analysis

The analysis was divided into three major sections:

### Univariate Analysis

Individual variables were analyzed to understand their distributions.

The analysis included:

1. Content Type Distribution
2. Release Year Analysis
3. Runtime Analysis
4. Genre Analysis
5. IMDb Score Distribution
6. TMDB Score Analysis
7. Age Certification Analysis

### Bivariate Analysis

Relationships between two variables were analyzed:

1. Content Type vs Runtime
2. Content Type vs IMDb Score
3. Genre vs IMDb Score
4. Release Year vs IMDb Score

### Multivariate Analysis

Relationships among multiple variables were analyzed:

1. IMDb Score vs IMDb Votes vs Content Type
2. Runtime vs IMDb Score vs Content Type
3. IMDb Score vs TMDB Popularity vs Content Type

---

## Key Findings

### Content Type

The final dataset contains:

- **8,511 Movies**
- **1,357 TV Shows**

Movies account for approximately **86.25%** of the dataset.

### Runtime

- Average runtime: approximately **85.98 minutes**
- Median runtime: **89 minutes**
- Movies generally have longer runtimes than TV Shows.

### IMDb Ratings

- Average IMDb score: approximately **5.98**
- IMDb scores range from approximately **1.1 to 9.9**
- TV Shows have a higher average IMDb score than Movies in this dataset.

### Genre and IMDb Score

Documentation and History are among the higher-rated genres by average IMDb score in the analyzed dataset.

### Release Year and IMDb Score

Average IMDb scores fluctuate across release years without a clear consistent upward or downward trend.

### IMDb Score and IMDb Votes

The correlation between IMDb Score and IMDb Votes is approximately **0.166**, indicating a weak positive relationship.

### Runtime and IMDb Score

The analysis does not show a strong direct relationship between runtime and IMDb score.

### TMDB Popularity and IMDb Score

The analysis does not show a strong direct relationship between TMDB popularity and IMDb score.

---

## Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Exploratory Data Analysis
- Statistical Descriptive Analysis

---

## Conclusion

The Exploratory Data Analysis provided a data-driven understanding of the Amazon Prime Movies and TV Shows content library.

The analysis found that Movies form the majority of the catalog, while TV Shows represent a smaller but distinct content category with different runtime and rating patterns.

Genre analysis indicated that informative and factual genres such as Documentation and History were among the higher-rated genres by average IMDb score in the analyzed dataset.

The analysis of release year showed fluctuations in average IMDb scores without a clear consistent trend.

The multivariate analysis showed that runtime and TMDB popularity do not display strong direct relationships with IMDb scores, while IMDb votes show only a weak positive relationship with IMDb scores.

Overall, the project demonstrates how Exploratory Data Analysis can be used to understand content characteristics, identify patterns, and support data-driven decisions related to content selection, acquisition, production, and audience engagement.
