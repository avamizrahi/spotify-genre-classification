# Spotify Genre Classification Using Machine Learning

## Overview
Multiclass classification project using Spotify audio features from 114,000+ tracks 
to predict musical genre. Built and compared multiple models to identify which audio 
characteristics best distinguish genres.

## Data
- 114,000 Spotify tracks across 20 genre categories
- Features: danceability, energy, acousticness, speechiness, instrumentalness, 
  valence, tempo, loudness, key, mode, liveness, time signature, popularity
- Similar genres combined prior to modeling (e.g. metal + metalcore, 
  pop + pop-film) to reduce overlap

## Methods
- **Multinomial Logistic Regression** (nnet) — primary model
- **Random Forest** — comparison model
- **Naive Bayes** — comparison model
- 70/30 train-test split
- Evaluated using accuracy, precision, F1 score, pseudo R-squared, 
  and confusion matrix

## Results
| Metric | Score |
|---|---|
| Accuracy | 35.69% |
| Precision | 29.97% |
| F1 Score | 27.82% |
| Pseudo R² | 0.308 |

Accuracy significantly exceeds the no-information rate of 12.47%, confirming 
meaningful signal in the audio features.

## Key Findings
- **Instrumentalness** and **speechiness** were the strongest predictors of genre
- Audio texture features (energy, danceability, acousticness) outperformed 
  musical attributes (key, tempo, popularity)
- Genres with distinct sonic profiles (metal, ambient, electronic/house) 
  were classified most accurately
- Broad genres like pop were harder to distinguish due to overlapping audio features

## Tools & Libraries
R, RMarkdown, tidyverse, nnet, caret, ggplot2
