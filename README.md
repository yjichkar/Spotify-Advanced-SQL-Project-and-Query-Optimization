# Spotify Advanced SQL Project and Query Optimization P-6

**Project Category**: Advanced  
[Download Dataset from Kaggle](https://www.kaggle.com/datasets/sanjanchaudhari/spotify-dataset)

![Spotify Logo](https://github.com/najirh/najirh-Spotify-Data-Analysis-using-SQL/blob/main/spotify_logo.jpg)

## 📖 Overview
This project focuses on analyzing a Spotify dataset using **SQL**. It covers the entire process from exploring and normalizing a denormalized dataset to writing SQL queries of varying complexity and optimizing their performance. The primary objectives are:

- Gain hands-on experience with advanced SQL techniques.
- Explore and understand real-world data related to music tracks, albums, and artists.
- Perform query optimization to improve database efficiency.
- Generate meaningful insights for data-driven decision-making.

---

## 🗂 Dataset Description
The dataset includes attributes such as:

- **Artist**: The performer of the track.
- **Track**: The name of the song.
- **Album**: The album where the track belongs.
- **Album Type**: Whether it’s a single or album.
- **Metrics**: danceability, energy, loudness, tempo, acousticness, instrumentalness, liveness, valence, and more.
- **Engagement**: Views, likes, comments, stream counts, etc.

---

## 📂 Project Workflow

### ✅ Step 1 – Data Exploration
- Review dataset attributes to understand track, album, and artist details.
- Explore metrics such as danceability, energy, loudness, and streaming numbers.
- Identify patterns and relationships that could be insightful for analysis.

### ✅ Step 2 – Data Preparation & Normalization
- Clean and structure the dataset.
- Normalize denormalized tables to optimize data integrity and querying.
- Insert data into the PostgreSQL database.

### ✅ Step 3 – Writing SQL Queries
- **Easy Queries**: Retrieve data, filter rows, and perform basic aggregations.
- **Medium Queries**: Use grouping, joins, and aggregate functions for deeper analysis.
- **Advanced Queries**: Implement nested queries, window functions, CTEs, and advanced data transformations.

### ✅ Step 4 – Query Optimization
- Analyze query performance using `EXPLAIN ANALYZE`.
- Apply indexing on frequently used columns such as `artist`.
- Refactor queries for faster execution and lower planning time.
- Evaluate results to ensure optimized data retrieval.

### ✅ Step 5 – Insights Generation
- Extract actionable insights from the data.
- Analyze user behavior and track popularity metrics.
- Apply best practices to improve data management and decision-making.

---

## 🧱 Database Setup

```bash
-- Drop existing table if exists
DROP TABLE IF EXISTS spotify;

-- Create the spotify table
CREATE TABLE spotify (
    artist VARCHAR(255),
    track VARCHAR(255),
    album VARCHAR(255),
    album_type VARCHAR(50),
    danceability FLOAT,
    energy FLOAT,
    loudness FLOAT,
    speechiness FLOAT,
    acousticness FLOAT,
    instrumentalness FLOAT,
    liveness FLOAT,
    valence FLOAT,
    tempo FLOAT,
    duration_min FLOAT,
    title VARCHAR(255),
    channel VARCHAR(255),
    views FLOAT,
    likes BIGINT,
    comments BIGINT,
    licensed BOOLEAN,
    official_video BOOLEAN,
    stream BIGINT,
    energy_liveness FLOAT,
    most_played_on VARCHAR(50)
);
