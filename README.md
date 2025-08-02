# Book Recommendation ML Model

This repository contains the machine learning model used for the **Book Recommendation API**.
Found here: https://github.com/Jason-Govender/Book-Archive

## Overview
The model clusters users based on their book ratings using **KMeans** and recommends top-rated books from similar users.  
It was trained on the Goodbooks 10K dataset and exports:
- `model.pkl` — the trained clustering model
- `scaler.pkl` — the fitted StandardScaler
- `top_books.pkl` — precomputed top books for each cluster

## Usage
The exported `.pkl` files are loaded in the API repository to serve real-time recommendations.

## Training
1. Load and clean the dataset.
2. Normalize user rating data with `StandardScaler`.
3. Fit a KMeans model with **50 clusters** (tuned for ~5,000 users).
4. Save the trained model and related artifacts to `.pkl` files.
