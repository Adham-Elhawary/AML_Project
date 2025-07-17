# 🎬 Movie Recommendation System

A hybrid movie recommendation system using **Content-Based Filtering**, **Collaborative Filtering (KNN & SVD)**, and their **Hybrid combination**. Built with the **MovieLens 20M Dataset** for personalized movie suggestions.

---

## 🔍 Project Overview

This project implements and compares three recommendation strategies:

- 🎯 **Content-Based Filtering**: Recommends movies based on metadata (genres, director, keywords).
- 👥 **Collaborative Filtering**: Recommends movies based on user rating patterns (KNN, SVD).
- ⚡ **Hybrid Approach**: Combines both methods using weighted scoring for better accuracy and personalization.

---

## 🧠 Algorithms & Techniques

### 1️⃣ Content-Based Filtering
- **Input**: Movie metadata (genre, description, keywords, director).
- **Method**: TF-IDF Vectorization + Cosine Similarity.
- **Output**: Top-N similar movies to a selected title.

### 2️⃣ Collaborative Filtering
- **Input**: User-movie rating matrix.
- **Methods**:
  - KNN (User-based or Item-based).
  - SVD (Singular Value Decomposition) using the Surprise library.
- **Output**: Predicted ratings for unseen movies.

### 3️⃣ Hybrid Model
- **Combination**: Weighted average of Content-Based and Collaborative predictions.
- **Tunable weights**: Example: `hybrid_score = 0.6 * SVD_score + 0.4 * content_score`.

---

## 🛠️ Setup Instructions

### ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/movie-recommender.git
   cd movie-recommender
data/
  ├── movies.csv
  ├── ratings.csv
  ├── links.csv
  └── tags.csv

