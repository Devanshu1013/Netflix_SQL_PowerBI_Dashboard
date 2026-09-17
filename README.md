# Netflix Shows & Movies Analysis (2022)

## Overview
This project analyzes Netflix's catalog of movies and TV shows using **PostgreSQL** for data querying, **Power Query** for data preparation, and **Power BI** for visualization. The dataset contains over **80,000 rows** combined across multiple Netflix data tables, sourced from Kaggle.

The goal is to build a scalable, high-quality analytical workflow that uncovers meaningful insights — genre preferences, title rankings, release trends, and viewer ratings — and present them through an interactive, mobile-friendly Power BI dashboard that Netflix stakeholders can explore on their own.

## Tools & Technologies
| Tool | Purpose |
|---|---|
| **PostgreSQL** | Storing the dataset and running SQL queries/subqueries for analysis |
| **Power Query** | Cleaning and transforming raw data before visualization |
| **Power BI** | Building interactive visuals and an end-to-end dashboard |

## Dataset
- **Source:** [Netflix TV Shows and Movies — Kaggle](https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies?select=titles.csv)
- **Size:** ~80,000+ combined rows
- **Key fields used:** title, type (MOVIE/SHOW), genres, release_year, imdb_score

## Dashboard
🔗 [View the interactive Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzIzYzcyY2YtMmNhOS00ODZiLTg1YTctOGMxYTEyNmNkYzJlIiwidCI6ImI5ZGYzOWRiLTM3NDUtNGZjOC04Y2EzLWVkNjFmNjkzOWMxMyIsImMiOjZ9)

The dashboard consolidates all SQL findings into visual, explorable charts covering:
- Movie vs. TV show counts
- Top and bottom 10 titles by IMDB score
- Most common genres across movies and shows
- Title distribution by decade
- Release-year trends, with a focused breakdown of 2019 (the peak release year)

It is designed to be mobile-friendly and interactive, allowing stakeholders to filter and drill into the data without needing to write SQL themselves.

## Analysis Steps

### Step 1 — Explore the Dataset
Establishes the baseline size of the catalog by counting how many entries are movies versus TV shows.

### Step 2 — Top 10 and Worst 10 Movies and TV Shows
Ranks titles by IMDB score to identify standout and underperforming content in both categories, informing recommendations and content strategy discussions.

### Step 3 — Top Genres for Movies and TV Shows
Identifies the most common genres separately for movies and TV shows, then combines both to find the top 3 genres overall. **Comedy** emerges as the most popular genre platform-wide, followed by Documentation and Drama.

### Step 4 — Number of Movies and TV Shows by Decade
Groups titles by release decade to show how Netflix's catalog has grown over time. Content volume increases sharply from the 2000s onward, with the 2010s alone contributing over 3,300 titles.

### Step 5 — Release Year Deep Dive
Counts titles per release year to find which year contributed the most content. **2019** stands out with 836 combined movie and TV show titles — the highest of any year.

### Step 6 — Release Year 2019 Deep Dive
Drills further into 2019 specifically:
- Identifies **Comedy** as the top genre that year (79 titles), reinforcing Comedy's platform-wide dominance.
- Lists all titles released in that top genre for 2019.
- Finds the highest-rated Comedy title of 2019: Dave Chappelle's *Sticks & Stones* (IMDB score: 8.4).

## Key Insights
- **Comedy is Netflix's most consistent top genre**, both overall and within specific years like 2019.
- **Content volume grew dramatically after 2010**, reflecting a deliberate platform strategy to scale its library.
- **2019 was Netflix's biggest release year** in this dataset, making it a useful case study for genre and rating trends.
- High and low IMDB-rated titles offer a data-backed starting point for recommendation and content-investment decisions.

## Repository Structure
```
├── README.md
├── Step 1.md          # Dataset exploration
├── Step 2.md          # Top/worst 10 titles
├── Step 3.md          # Genre analysis
├── Step 4.md          # Titles by decade
├── Step 5.md          # Release year analysis
├── Step 6.md          # 2019 deep dive
└── images/            # SQL query result screenshots
```

Each `Step` file contains the SQL question being answered, the query itself, a screenshot of the query result, and a written interpretation of the findings.
