# Filtering Data with SQL - Lab

## Introduction 

NASA wants to go to Mars! Before they build their rocket, NASA needs to track information about all of the planets in the Solar System. In this lab, you'll practice querying the database with various `SELECT` statements. This will include selecting different columns and implementing other SQL clauses like `WHERE` to return the data desired.

<img src="https://raw.githubusercontent.com/learn-co-curriculum/dsc-filtering-lab-v2-4/master/images/planets.png" alt="image of solar system" width="600">

## Objectives

You will practice the following:

* Retrieve a subset of records from a table using a `WHERE` clause
* Filter results using conditional operators such as `BETWEEN`, `IS NULL`, and `LIKE`
* Apply an aggregate function to the result of a filtered query

## Connecting to the Database

To get started, import `sqlite3` as well as `pandas` for conveniently displaying results. Then, connect to the SQLite database located at `planets.db`. 


```python
# Your code here
```

## Database Schema

This database contains a single table, `planets`. This is the schema:

```
CREATE TABLE planets (
  id INTEGER PRIMARY KEY,
  name TEXT,
  color TEXT,
  num_of_moons INTEGER,
  mass REAL,
  rings BOOLEAN
);
```

The data looks something like this:

| id | name    | color      | num_of_moons | mass   | rings |
| -- | ------- | ---------- | ------------ | ------ | ----- |
| 1  | Mercury | gray       | 0            | 0.55   | FALSE |
| 2  | Venus   | yellow     | 0            | 0.82   | FALSE |
| 3  | Earth   | blue       | 1            | 1.00   | FALSE |
| 4  | Mars    | red        | 2            | 0.11   | FALSE |
| 5  | Jupiter | orange     | 67           | 317.90 | FALSE |
| 6  | Saturn  | hazel      | 62           | 95.19  | TRUE  |
| 7  | Uranus  | light blue | 27           | 14.54  | TRUE  |
| 8  | Neptune | dark blue  | 14           | 17.15  | TRUE  |

