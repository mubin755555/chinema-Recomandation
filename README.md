
# Cinema Recommendation System

This repository contains a data analysis project for building a cinema recommendation system, developed as part of a university lab project. The goal of this project is to analyze movie data and build a recommendation system that suggests movies based on various features such as genre, popularity, ratings, etc. This project was completed using Jupyter Notebook, leveraging libraries such as pandas, numpy, and scikit-learn.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Analysis and Model](#data-analysis-and-model)
- [Results and Insights](#results-and-insights)
- [Technologies Used](#technologies-used)
- [Usage](#usage)
- [Optional Extension](#optional-extension)
- [Conclusion](#conclusion)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This project aims to analyze and process a dataset of movies to provide a recommendation system. The recommendation model is built based on features such as genres, popularity scores, and other attributes. The project involves data preprocessing, feature engineering, and implementing recommendation algorithms.

## Dataset
The dataset, `tmdb_5000_movies.csv`, contains various attributes related to movies:
- **Title**: Movie title
- **Genres**: Genres of the movie
- **Popularity**: Popularity score of the movie
- **Vote Average**: Average rating given to the movie
- **Vote Count**: Number of votes received
- **Overview**: Brief description of the movie
- **Release Date**: Release date of the movie
- **Other Features**: Various other metadata attributes

This dataset serves as the basis for building content-based or hybrid recommendation models.

## Data Analysis and Model
1. **Data Cleaning**: Handle missing values and remove or transform irrelevant data.
2. **Feature Engineering**: Process and structure features like genres and keywords for model input.
3. **Model Selection**: Implement a **Content-Based Recommendation** model using cosine similarity, and explore other recommendation techniques if possible.
4. **Evaluation**: Assess recommendation accuracy and relevance based on user similarity metrics.

## Results and Insights
- **Top Recommendations**: Provides a list of movies that are closely related based on genres and popularity.
- **User Preferences**: Insight into the patterns and types of movies that are commonly liked based on user or item features.

## Technologies Used
- **Python**: Programming language for analysis and modeling.
- **Pandas**: Data manipulation and analysis.
- **Numpy**: Numerical operations.
- **Scikit-learn**: Machine learning and similarity measures.
- **Jupyter Notebook**: Development platform.

  ## Step 2: Load the Dataset
  movies = pd.read_csv('tmdb_5000_movies.csv')
movies.head()
## Step 3: Data Cleaning
movies.dropna(subset=['genres', 'overview'], inplace=True)
## Step 4: Feature Engineering
# Example code for extracting genres
movies['genres'] = movies['genres'].apply(lambda x: ' '.join([genre['name'] for genre in eval(x)]))
## Step 5: Model Implementation

from sklearn.feature_extraction.text import CountVectorizer
count = CountVectorizer(stop_words='english')
count_matrix = count.fit_transform(movies['genres'])

cosine_sim = cosine_similarity(count_matrix, count_matrix)
def get_recommendations(title, cosine_sim=cosine_sim):
    # Example function code here

## Step 6: Testing the Recommendation System

get_recommendations('The Godfather')

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/mubin755555/cinema-recommendation.git
## Acknowledgements

- [SabrinaAkter1](https://github.com/SabrinaAkter1)

   
