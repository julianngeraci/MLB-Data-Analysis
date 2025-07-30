## MLB Team Report Generator -- MLBStats.ipynb

This Python script generates visual performance reports for every MLB team from 1998 to 2024, saving them as PNG files.

###  What It Does

- Loads team statistics from a CSV file (`mlb_1998_2024.csv`)
- Standardizes old franchise names (e.g., "Montreal Expos" → "Washington Nationals")
- Computes additional metrics:
  - Win percentage
  - Run differential
- Skips 2020 due to the shortened season
- For each team:
  - Creates a correlation matrix heatmap
  - Creates a 2×2 subplot showing team performance over time
- Saves both charts as PNGs in a folder called `team_reports/`

### Output

Each team will have two files saved in `team_reports/`:

- `{TeamName}_corr.png`: Correlation matrix
- `{TeamName}.png`: Multi-panel performance summary
