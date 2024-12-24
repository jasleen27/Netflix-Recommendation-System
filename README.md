# Netflix Recommendation System

This project implements a content-based recommendation system using machine learning techniques. The system clusters Netflix movies based on various features such as genre, director, and cast, and provides personalized recommendations to users. It utilizes algorithms like K-Means clustering, Agglomerative Hierarchical clustering, and cosine similarity to generate the suggestions.

## Table of Contents

- [Project Objective](#project-objective)
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Pipeline](#data-pipeline)
- [Conclusion](#conclusion)
- [Usage](#usage)
- [Acknowledgements](#acknowledgements)

## Project Objective
The objective of this project is to develop a content-based recommendation system for Netflix movies and TV shows using machine learning techniques, such as clustering and cosine similarity, to provide personalized movie recommendations.

## Project Overview

This Netflix recommendation system leverages machine learning algorithms to classify and recommend Netflix shows. The key steps include:
- **Data Preprocessing**: Clean and preprocess raw data.
- **Exploratory Data Analysis (EDA)**: Analyze trends and features.
- **Clustering**: Group similar shows using K-Means and Agglomerative clustering.
- **Content-Based Recommendation**: Use cosine similarity to recommend movies based on user preferences.

## Dataset

The dataset is collected from Flixable, a third-party Netflix search engine. This dataset consists of TV shows and movies available on Netflix as of 2019. It includes over 7787 records and 12 attributes. Each attribute provides detailed information about the movies/TV shows. More details of the dataset can be found on the [Kaggle website](https://www.kaggle.com/datasets/sambhajizambre/netflix-movies-and-tv-shows-clustering?select=netflix_titles.csv).

## Data Pipeline

### 1. Analyze Data:
In this initial step, we analyzed various features of the dataset. We examined the shape of the data, the data types of each feature, and the statistical summary to better understand the structure and characteristics of the dataset.

### 2. EDA:
Exploratory Data Analysis (EDA) is crucial for understanding the patterns and relationships within the data. During EDA, we observed trends and dependencies that were helpful for further data processing.

### 3. Data Cleaning:
Data cleaning involved checking for duplicate entries, handling missing values by replacing them with empty strings or dropping rows, and detecting and treating outliers to ensure clean and usable data.

### 4. Textual Data Preprocessing:
For clustering, we preprocessed the data based on the following attributes: director, cast, country, genre, rating, and description. This stage involved:
- Removing stop words and punctuation marks
- Converting all textual data to lowercase
- Stemming words to generate meaningful roots
- Tokenizing the corpus and performing word vectorization

Principal Component Analysis (PCA) was used to reduce dimensionality and handle the curse of dimensionality.

### 5. Clusters Implementation:
We applied K-Means and Agglomerative Hierarchical clustering algorithms to group the movies into clusters. The optimal number of clusters was determined using techniques like the elbow method and silhouette score analysis.

### 6. Build Content Based Recommendation System:
A content-based recommender system was built using the similarity matrix obtained from cosine similarity. This system recommends 10 movies or shows based on the type of movie/show the user has watched.

## Usage
1. Clone the repository.
2. Install the required dependencies.
3. Run the `Netflix_Recommendation_System.ipynb` notebook to explore the analysis, clustering, and recommendation system.

## Conclusion

In this project, we worked on a text clustering problem where we aimed to classify and group Netflix shows into clusters such that the shows within a cluster are similar to each other, and those in different clusters are dissimilar. The process involved the following steps:

- **Data Cleaning & EDA**: Addressed missing values, identified trends, and explored the data.
- **Textual Data Preprocessing**: Preprocessed and vectorized the textual data using TFIDF.
- **Dimensionality Reduction**: Used PCA to reduce the number of features to a manageable level.
- **Clustering**: Used K-Means clustering to group similar shows.
- **Recommendation System**: Built a content-based recommendation system based on cosine similarity.

The optimal number of clusters was found to be 4, and the recommender system successfully recommended shows based on the user's viewing preferences.

## Acknowledgements
- Dataset from [Kaggle Netflix Dataset](https://www.kaggle.com/datasets/sambhajizambre/netflix-movies-and-tv-shows-clustering)


