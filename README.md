# Movie Recommendation System

**Author:** Logan Laszewski

**Project Type:** Data Analysis, Recommendation Systems, Python

**Last Updated:** November 2025

---

## Overview

The Movie Recommendation System is a Python-based collaborative filtering project designed to generate personalized movie suggestions using the MovieLens 32M dataset.

The system analyzes a user’s movie ratings, identifies similar users through correlation-based similarity, and recommends films that those similar users enjoyed. This project demonstrates similarity analysis, large-scale data wrangling, fuzzy matching, and building a full recommendation pipeline using statistical techniques.

---

## Why This Project?

Most recommendation systems optimize for engagement, not genuine preference. Platforms like Netflix and Spotify rely on clicks, watch time, and completion rate; signals that often blur the line between what we consumed and what we truly enjoyed.

Instead of inferring taste from behavior, the system uses explicit movie ratings and transparent similarity logic. By comparing your ratings with those of people who rate films like you do, the system uncovers recommendations grounded in shared taste.

Collaborative filtering works because people with similar rating patterns tend to enjoy similar movies. This system makes that logic visible and interpretable. Every recommendation can be traced back to specific users, their ratings, and how closely their preferences align with yours.

---

## Features

### Personalized Recommendation Engine

* Users enter 8–20 movies and rate them on a 1–5 scale.

* The system:

  * Finds MovieLens users who rated ≥70% of the same movies

  * Computes Pearson correlation to measure similarity

  * Selects the top 10 “taste neighbors”

  * Recommends films those neighbors rated highly

* No machine learning training required — purely statistical and data-driven.

### Fuzzy Title Matching (RapidFuzz)

* Handles natural, imperfect, or partial title input.

* Matches entries like “Knives Out Mystery” to “Glass Onion: A Knives Out Mystery (2022)”.

* Improves accuracy and user experience.

### Large Scale Dataset Support

* Uses MovieLens 32M (32M ratings, 87k+ movies).

* Automatic download and extraction on first run (And supports manual upload of movies.csv and ratings.csv.).

### Mainstream Bias Correction

* Applies a gentle popularity penalty so recommendations surface more interesting, less obvious titles.

* Prevents lists dominated by well-known blockbusters.

---

## Technical Details

### Languages & Libraries:

* Python, Pandas, NumPy

* SciPy (Pearson correlation)

* RapidFuzz for fuzzy matching

* urllib, zipfile, os for dataset handling

---

## Recommendation Workflow

1. Dataset Setup

 * Download or load movies.csv and ratings.csv from the MovieLens 32M dataset.

 * Merge movie info and ratings into a single dataset.

2. User Input Collection

 * User enters 8–20 movies with ratings.

 * Fuzzy matching ensures correct title identification.

3. Find Similar Users

 * Identify MovieLens users with at least 70% overlap in rated movies.

 * Filter down to meaningful comparison sets.

4. Compute Similarity

 * Use Pearson correlation to measure rating agreement.

 * Retain the top 10 positively correlated users.

5. Generate Recommendations

* Recommend movies:

 * Not yet rated by the user

 * Rated by at least 4 neighbors

 * With high similarity weighted scores

---

##  Project Learnings

* Built a complete recommendation pipeline using statistical methods.

* Implemented Pearson correlation for user similarity scoring.

* Improved usability with fuzzy matching and mainstream bias adjustments.

* Explored real recommendation system logic used by streaming platforms.

## Future Enhancements

* Build a Streamlit or web interface for interactive recommendations.

* Integrate content based features (genres, tags) for hybrid recommendations.

* Add AI integration in some form to improve the recommendation system.

---

## App
- Colab demo: [Script](https://github.com/Logan142414/MarchMadness2025Model/blob/main/MarchMadness_Data_Science.ipynb)

---
  
## Medium Article
- [How to Build a Movie Recommender That Actually Understands Your Taste](https://medium.com/@logan.laszewski14/movie-recommendation-system-56c4a8c53ab4)


