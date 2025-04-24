# 🎬 Movie Recommendation System using SVD  
A collaborative filtering-based movie recommender built on the **MovieLens 25M** dataset using **Singular Value Decomposition (SVD)**, enhanced with metadata and visualization features.

---

## 📌 Project Overview

This project demonstrates how to build a personalized movie recommendation system using SVD.  
We use real-world user ratings from the [MovieLens 25M](https://grouplens.org/datasets/movielens/25m/) dataset and enhance it with tag relevance metadata and visual explanations.

---

## 🧠 Key Objectives

- Load and preprocess a massive real-world dataset
- Handle common issues like cold-start users and movie sparsity
- Train an SVD-based collaborative filtering model
- Evaluate model accuracy using RMSE and MAE
- Generate personalized movie recommendations
- Integrate metadata and poster images from TMDB
- Visualize latent features to interpret model behavior

---

## 🛠️ Technologies Used

- Python 3.10+
- [scikit-surprise](https://surprise.readthedocs.io/en/stable/)
- NumPy, pandas, matplotlib, seaborn
- scikit-learn (for metrics)
- TMDB API (for movie posters)

---

## 🧹 Data Preprocessing

- Filtered users and movies with fewer than 5 ratings to avoid cold-start issues
- Merged genome tag data to enrich movie metadata
- Performed **time-based split** (train/validation/test) to simulate real-world behavior

---

## 🧮 Model: Singular Value Decomposition (SVD)

We use the `SVD()` model from the `surprise` library.  
SVD factorizes the user-item matrix into latent features that capture hidden relationships — such as preferences for genre, style, or tone.

> 🎯 Trained on 70% of the data  
> 🧪 Validated on 15%  
> ✅ Tested on 15% with full batch evaluation

---

## 📊 Evaluation

We evaluated model performance using:
- **RMSE**: Root Mean Squared Error  
- **MAE**: Mean Absolute Error

Evaluation was done in **batches** to support full test set performance without memory crashes.

---

## 📈 Visualizations

- Latent features of movies visualized using heatmaps
- Recommendations displayed with predicted ratings and movie details
- Posters fetched using TMDB API

---

## 🎁 Recommendation Generation

- For any given user, we:
  - Exclude movies they’ve already rated
  - Predict ratings for unseen movies
  - Rank and display top recommendations
- Sample user history and predicted movies shown with:
  - Title
  - Genres
  - Poster image

   

