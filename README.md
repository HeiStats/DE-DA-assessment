# Data Analysis Mentorship Assessment

## Objective

Assess the candidate’s ability to integrate SQL, Python, Docker, and GitHub in a realistic data analysis workflow.

## Scenario

You are hired as a `Junior Data Analyst` in a small analytics startup.
The startup stores data in a `PostgreSQL` database, performs analysis in `Python`, and manages projects using `Docker` and `GitHub`.

You are required to:

1. Set up a local development environment using Docker.

2. Load a dataset into a PostgreSQL database.

3. Run analysis using Python.

4. Version control your project on GitHub.

---------------------------------------------------------

## Part 1 — Setup (Docker & GitHub)

1. Create a new GitHub repository named data-analysis-assessment.

    - Include a proper README.md describing the project steps.

    - Use clear commit messages for every stage.

2. Create a docker-compose.yml file that defines:

    - A PostgreSQL service (e.g., postgres:15).

    - A Python service (use an image like python:3.11).

    - The two containers should be on the same network.

3. Ensure PostgreSQL is accessible via port 5432 and create a database named assessment_db.

4. Mount a local src/ directory into the Python container so your scripts can run inside Docker.

-----------------------------------------------------------

## Part 2 — Data Loading (SQL & Python)

1. Download a dataset (e.g., from Kaggle
 or use this open dataset on [global food prices](https://www.kaggle.com/datasets/jocelyndumlao/global-food-prices/croissant/download)
).

    - Save it as data.csv inside your project folder.

2. Write a Python script (src/load_data.py) that:

    - Connects to PostgreSQL (using psycopg2 or sqlalchemy).

    - Creates a SQL table with appropriate data types.

    - Loads data from data.csv into the table.
    
3. Write SQL queries to:

    - Count total records.

    - Identify missing values.

    - Compute summary statistics (min, max, avg) for numerical columns.

Store all SQL queries in a queries.sql file.

----------------------------------------------------

## Part 3 — Data Analysis (Python + SQL Integration)

1. Create another Python script (`src/analyze_data.py`) that:

    - Connects to `PostgreSQL`.

    - Executes some analytical queries (e.g., grouping, filtering).

    - Returns a Pandas DataFrame for analysis.

2. Perform at least two visualizations (e.g., using matplotlib or seaborn):

    - A bar chart of one categorical variable.

    - A trendline of a numerical variable over time.

3. Save the final analysis outputs (e.g., plots or CSV summary) in an outputs/ folder.

-------------------------------------

## Part 4 — Deliverables

Submit the GitHub repository link containing:

    - docker-compose.yml

    - src/load_data.py

    - src/analyze_data.py

    - queries.sql

    - data.csv (or link to dataset)

    - README.md (clearly document setup and run steps)
