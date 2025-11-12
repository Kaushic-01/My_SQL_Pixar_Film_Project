#  Pixar Film Analysis – MySQL Project

## Project Overview

This **MySQL project** presents a comprehensive **data analysis of Pixar films**, exploring various aspects such as **box office performance**, **critical and audience reception**, **genres**, and **Academy Award recognition**.

The SQL script contains **well-structured and documented queries** designed to deliver valuable insights into Pixar’s filmography.
It serves as an excellent resource for anyone learning **SQL data analysis**, **advanced querying**, or exploring **film analytics** using real-world datasets.

---

##  Objectives

* Analyze **box office performance** across all Pixar films.
* Compare **Rotten Tomatoes**, **Metacritic**, and **Audience Scores** to assess film reception.
* Identify **directors with multiple films** and calculate their total revenue.
* Explore **genres and sub-genres**, and evaluate **average gross and runtime** by film rating.
* Examine **Academy Award trends**, including nominations, wins, and profitability analysis.

---

##  Database & Tables

**Database Name:** `Pixar_Db`

Key tables used in the project:

* **pixar_films** – Film titles, release dates, runtime, and ratings.
* **box_office** – Budget, worldwide gross, and profitability data.
* **genres** – Genres and sub-genres for each film.
* **public_response** – Rotten Tomatoes, Metacritic, and Audience scores.
* **pixar_people** – Directors, producers, and credited personnel.
* **academy** – Awards, nominations, and achievements data.

---

##  Analysis Summary

###  Box Office Performance

* Identify **highest-grossing films** and calculate **average worldwide gross by genre**.
* Measure **profitability** using `(worldwide gross – budget)`.
* Rank films by worldwide gross using **window functions (RANK())**.

###  Critical & Audience Reception

* Compare **Rotten Tomatoes** and **Metacritic** scores.
* Find films with **scores above 90%** on both critic and audience scales.
* Identify **directors with the highest average audience score**.

###  Film & People Data

* List **directors and their films**, and count those who directed multiple projects.
* Find the **most credited people** per film.
* Analyze total revenue generated per director.

###  Award Recognition

* Count **Academy Award wins and nominations** for each film.
* Identify **films with multiple wins or nominations but no wins**.
* Calculate **average scores for award-winning films**.

###  Genre & Film Attributes

* Explore **unique genres and sub-genres**.
* Determine **average runtime by film rating**.
* Analyze **films released by decade** and their box office trends.

---

##  Advanced SQL Techniques

This project uses a variety of **advanced SQL concepts**:

* **Joins** – Combining multiple tables for complete insights.
* **Subqueries** – Extracting nested results for comparisons.
* **Window Functions** – Using `RANK()`, `LEAD()`, and rolling averages.
* **Conditional Aggregation** – Counting awards by win/nominated status.
* **Data Cleaning** – Using `ALTER TABLE`, `UPDATE`, and `STR_TO_DATE()`.

---

##  Tools & Technologies

* **MySQL Workbench / XAMPP / phpMyAdmin** – Database environment
* **SQL** – Query language for analysis and transformations
* **Excel / CSV** – For data preparation and visualization exports

---

##  Sample Query Insights

| Query Topic               | Example SQL Functionality                                     |
| ------------------------- | ------------------------------------------------------------- |
| Highest-Grossing Film     | `ORDER BY box_office_worldwide DESC LIMIT 1`                  |
| Award-Winning Films       | `GROUP BY film HAVING total_wins >= 2`                        |
| Top Directors             | `COUNT(film) HAVING number_of_films > 1`                      |
| Audience vs Critic Scores | `SELECT film, audience_score, rotten_tomatoes_score`          |
| Profitability Ranking     | `RANK() OVER (ORDER BY (box_office_worldwide - budget) DESC)` |

---

##  How to Use

1. **Clone this repository** to your system.
2. Open MySQL Workbench or any SQL IDE.
3. Execute the provided SQL script:

   ```sql
   SOURCE Pixar_Film_Analysis.sql;
   ```
4. Explore queries to understand Pixar film trends, performance, and awards.
5. Modify filters (e.g., year, genre, director) for custom analysis.

---

##  Learning Outcomes

Through this project, you’ll learn to:

* Apply **real-world SQL analysis** on structured datasets.
* Use **window functions** and **aggregate analysis** in MySQL.
* Derive actionable insights from **cinema and entertainment data**.
* Design **data-driven reports** using only SQL logic.

---

##  Next Steps / Future Enhancements

Potential areas to extend this project:

* **Integrating Tableau or Power BI** for visual dashboards
* **Building Stored Procedures and Views** for modular queries
* **Creating an ETL Pipeline** to automate Pixar data updates
* **Incorporating Machine Learning Models** for film success prediction
* **Adding JSON or API Integration** for real-time box office data
* **Normalizing Database Design** for scalability and optimization
* **Performing Correlation Analysis** between budget, ratings, and revenue
* **Developing a Python or Flask App** for interactive SQL query results
* **Adding Index Optimization** for performance tuning
* **Using CTEs (Common Table Expressions)** for cleaner complex queries

---

## 👤 Author

**Kaushic Krishnamurthy G**
 [kaushickrishnamurthy@gmail.com](mailto:kaushickrishnamurthy@gmail.com)
 Data Analyst | SQL Developer | Business Intelligence Enthusiast

---

##  License

This project is open-source and available under the [MIT License](LICENSE).

---

##  Acknowledgements

* Pixar film data adapted for educational and analytical purposes.
* Inspired by movie analytics and SQL learning initiatives.
