# MLB Team Report Generator — MLBStats.ipynb

This Python notebook generates visual performance reports for every MLB team from 1998 to 2024, saving the results as PNG files.

## What It Does

- Loads team statistics from a CSV file (`mlb_1998_2024.csv`)
- Standardizes franchise names to current versions (e.g., "Montreal Expos" → "Washington Nationals")
- Computes key metrics:
  - Win percentage
  - Run differential
- Skips the 2020 season due to its shortened length
- For each team:
  - Creates a correlation matrix heatmap of relevant stats
  - Creates a 2×2 subplot summarizing team performance trends over time
- Saves generated charts as PNG files in a directory called `team_reports/`

## Output

Each team has two output files saved in `team_reports/`:

- `{TeamName}_corr.png`: Correlation matrix heatmap
- `{TeamName}.png`: Multi-panel performance summary plot

---

# MLB Team Report Generator — MLBSQL.ipynb

This Python notebook builds on MLBStats.ipynb by loading the data into a SQLite database and performing advanced SQL-based analyses.

## What It Does

- Loads the cleaned MLB dataset into an in-memory SQLite database
- Standardizes team names for consistency
- Merges MLB data with World Series winner data to flag championship teams
- Enables interactive SQL queries for:
  - Retrieving team stats by name and year
  - Ranking teams by various statistics within a season
  - Analyzing which regular-season stats best predict World Series winners using SQL window functions
- Calculates and prints the accuracy of stats like winning percentage, runs scored, and run differential in identifying World Series champions
- Generates bar charts visualizing top teams by selected stats and predictive accuracy

## Output

- Flagged dataset with World Series winners saved as `mlb_with_ws_flag.csv`
- Tables summarizing how often each stat’s top-ranked teams included the World Series champion
- Visualizations such as bar charts showing stat predictive power

