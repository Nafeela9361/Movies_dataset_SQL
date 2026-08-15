# 🎬 Movie Collection SQL Project

## 📌 Project Overview

This project is a **Movie Collection Database** developed using **MySQL**. It demonstrates how to organize movie-related data using relational database concepts, including **actors, directors, languages, and movies**.

The project uses separate master tables for actors, directors, and languages, and connects them to the movie details table using **Primary Keys and Foreign Keys**.

## 🛠️ Technologies Used

* **Database:** MySQL
* **Language:** SQL
* **Concepts:** Relational Database, Primary Key, Foreign Key, Joins, Filtering, Sorting, Aggregation, Group By, Having, Distinct, Like, Between, Limit

## 🗂️ Database Structure

The database is named:

`MOVIE_COLLEC`

### Tables

#### 1. ACT_MAST

Stores unique actor information.

| Column   | Description     |
| -------- | --------------- |
| ACT_ID   | Unique actor ID |
| ACT_NAME | Actor name      |

#### 2. DIR_MAST

Stores unique director information.

| Column   | Description        |
| -------- | ------------------ |
| DIR_ID   | Unique director ID |
| DIR_NAME | Director name      |

#### 3. LANG_MAST

Stores unique movie languages.

| Column  | Description        |
| ------- | ------------------ |
| LANG_ID | Unique language ID |
| LANG    | Language name      |

#### 4. MOV_DETAILS

Stores movie information and connects actors, directors, and languages using foreign keys.

| Column   | Description        |
| -------- | ------------------ |
| REL_YEAR | Movie release year |
| MOV_NAME | Movie name         |
| ACT_ID   | Actor reference    |
| DIR_ID   | Director reference |
| LANG_ID  | Language reference |

## 🔗 Database Relationships

The project follows a relational database structure:

```text
ACT_MAST
   │
   │ ACT_ID
   ▼
MOV_DETAILS
   ▲
   │ DIR_ID
DIR_MAST

MOV_DETAILS
   │
   │ LANG_ID
   ▼
LANG_MAST
```

* `ACT_MAST.ACT_ID` → `MOV_DETAILS.ACT_ID`
* `DIR_MAST.DIR_ID` → `MOV_DETAILS.DIR_ID`
* `LANG_MAST.LANG_ID` → `MOV_DETAILS.LANG_ID`

## 📊 SQL Operations Covered

The project contains **28 SQL queries** covering different database operations.

### 🔍 Data Retrieval

* Display all movie details
* Display movie names and actors
* Find movies released in a specific year
* Find movies acted by a specific actor
* Find movies directed by a specific director
* Filter movies by language

### 🎯 Filtering

* `WHERE`
* `LIKE`
* `BETWEEN`
* `DISTINCT`

### 📈 Sorting

* Sort movies by release year
* Sort movies alphabetically by movie name
* Find the latest 10 movies
* Find the earliest 10 movies

### 📊 Aggregation

The project uses:

* `COUNT()`
* `GROUP BY`
* `HAVING`
* `ORDER BY`
* `LIMIT`

Examples include:

* Total number of movies
* Movies released in each language
* Movies acted by each actor
* Movies directed by each director
* Movies released each year
* Year with the highest number of releases
* Actor with the most movies
* Director with the most films
* Actors working in more than 3 languages

## 💡 Key SQL Concepts Demonstrated

### Primary Keys

Unique identifiers are created for actors, directors, and languages using `AUTO_INCREMENT`.

### Foreign Keys

The `MOV_DETAILS` table uses foreign keys to establish relationships with the master tables.

### INNER JOIN

Multiple tables are joined to retrieve complete movie information.

### GROUP BY

Used to categorize and count movies by:

* Language
* Actor
* Director
* Release year

### HAVING

Used to filter grouped results, such as actors who worked in more than 10 movies.

## 🎯 Project Objectives

* Understand relational database design.
* Practice creating databases and tables.
* Learn how to establish table relationships.
* Apply Primary Keys and Foreign Keys.
* Perform data retrieval using SQL.
* Practice different types of filtering and sorting.
* Analyze movie data using aggregate functions.
* Develop practical experience with SQL joins and grouping.

## 📚 Learning Outcomes

Through this project, I gained practical experience in:

* **MySQL database creation and management**
* **Database normalization concepts**
* **Primary and Foreign Key relationships**
* **INNER JOIN operations**
* **Data filtering and sorting**
* **Aggregate functions**
* **GROUP BY and HAVING**
* **SQL data analysis**
* **Relational database design**

## 📁 Project Structure

```text
Movie-Collection-SQL/
│
├── Movie_Collection.sql
├── README.md
└── screenshots/
    └── query-results/
```

## 🚀 How to Run the Project

1. Open **MySQL Workbench**.
2. Create/open the SQL script.
3. Execute the movie data insertion queries.
4. Execute the database and table creation queries.
5. Run the SQL queries individually to explore the results.

> **Note:** The original `MOVIES` table must contain the movie data (`REL_YEAR`, `MOV_NAME`, `ACT_NAME`, `LANG`, and `DIR_NAME`) before populating the master tables.

## 👩‍💻 Author

**Nafeela Beer**

Aspiring **Generative AI / AI & ML Professional** with an interest in SQL, Data Analytics, NLP, and Generative AI.
