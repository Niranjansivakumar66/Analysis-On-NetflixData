# 🎬 Netflix Data Analysis

A data cleaning and exploratory data analysis (EDA) project on the Netflix titles dataset, answering real-world business questions about content trends, directors, ratings, and more.

## 📖 Overview

This project explores the Netflix Movies and TV Shows dataset to uncover patterns in content type, release trends, country-wise availability, ratings, and cast/director contributions. It follows a structured process — starting with data cleaning (duplicates, nulls) and moving through a series of guided analytical questions, each answered with pandas and visualized where relevant.

## 📊 Dataset

- **File expected:** `8. Netflix Dataset.csv`
- **Key columns used:** `Show_Id`, `Category`, `Title`, `Director`, `Cast`, `Country`, `Release_Date`, `Rating`, `Duration`, `Type`
- Place the CSV in the same directory as the notebook, or update the file path in the notebook to match your setup.

## 🛠️ Requirements

- Python 3.x
- pandas
- seaborn
- matplotlib (used implicitly via `.plot()`)

Install dependencies with:
```bash
pip install pandas seaborn matplotlib
```

## 🔍 Workflow

The notebook (`Analysis_on_Netflixdata.ipynb`) is structured in two phases:

### 1. Data Cleaning
- Loads the dataset and inspects its shape, size, and structure (`info()`, `dtypes`).
- Identifies and removes duplicate rows.
- Checks for missing values across all columns and visualizes them with a null-value heatmap (seaborn).
- Converts the `Release_Date` column into a proper datetime format (`New_Date`) for time-based analysis.

### 2. Exploratory Analysis (Q&A Format)
The analysis is driven by a series of business questions, including:

| # | Question |
|---|----------|
| Q1 | Show ID and director of *House of Cards* |
| Q2 | Distribution of TV shows/movies by release year |
| Q3 | Total count of Movies vs. TV Shows |
| Q4 | All movies released in a given year |
| Q5 | Titles of all movies released in India |
| Q6 | Top 10 directors by number of titles |
| Q7 | Records filtered by category, genre, and country |
| Q8 | Movies/shows featuring Tom Cruise |
| Q9 | Unique content ratings defined by Netflix |
| Q9.1 | Count of TV-14 rated movies in Canada |
| Q9.2 | Count of R-rated TV shows released after 2018 |
| Q10 | Maximum duration among movies/shows |

Each question is answered using pandas filtering, grouping, and string operations, with bar charts used to visualize distributions (e.g., titles by release year, Movies vs. TV Shows).

## 📈 Key Insights

- Netflix's content library is split between Movies and TV Shows, with a visible skew depending on release year.
- Certain directors have contributed disproportionately more titles than others.
- Content ratings vary significantly by country (e.g., TV-14 ratings in Canada).
- Duration formats differ between Movies (minutes) and TV Shows (seasons), requiring format parsing before numerical analysis.

## 🚀 How to Run

1. Place `8. Netflix Dataset.csv` in the project directory.
2. Install the required dependencies.
3. Open the notebook in Jupyter:
   ```bash
   jupyter notebook Analysis_on_Netflixdata.ipynb
   ```
4. Run all cells in order — the data cleaning steps must execute before the analysis questions.

## 🔮 Possible Improvements

- Split the combined `Duration` column more robustly to handle both "X min" (movies) and "X Season(s)" (TV shows) formats separately.
- Replace static `.plot(kind="bar")` calls with more polished visualizations (e.g., Seaborn/Plotly) with titles, labels, and consistent styling.
- Add a summary dashboard consolidating all Q&A insights into a single visual report.

## 📝 License

This project is intended for educational and portfolio purposes.
