# Movie Recommendation System 🎬

A content-based Movie Recommendation System built using Python and Machine Learning techniques. This project recommends movies similar to a user's selected movie by analyzing movie information such as genres, keywords, overview, cast, and director.

The system uses Natural Language Processing (NLP), Bag of Words vectorization, and Cosine Similarity to identify and recommend similar movies.

## 📌 Project Overview

The Movie Recommendation System analyzes movie metadata and generates recommendations based on similarities between movies.

It combines different movie attributes into a single text-based feature called **tags**, processes the text using stemming, converts it into numerical vectors, and calculates cosine similarity to find movies with similar content.

For example, when a user selects *Fight Club*, the system recommends five movies with similar content characteristics.

## 🛠️ Technologies & Libraries

The following technologies and Python libraries are used in this project:

- **Python** – Programming language
- **Pandas** – Data manipulation and preprocessing
- **NumPy** – Numerical computing library
- **NLTK** – Natural Language Processing and stemming
- **Scikit-learn** – Text vectorization and similarity calculation
- **KaggleHub** – Downloading the movie dataset

## 📂 Dataset

This project uses the **TMDB 5000 Movie Dataset**, available on Kaggle.

Dataset: [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

The dataset contains two CSV files:

- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

Both datasets are merged using the movie title.

The following features are selected for building the recommendation system:

- Movie ID
- Movie Title
- Genres
- Keywords
- Overview
- Cast
- Crew (Director)

## ⚙️ Project Workflow

The project follows these major steps:

### 1. Data Collection

- Download the TMDB 5000 Movie Dataset using KaggleHub.
- Load both CSV files using Pandas.
- Merge the movie and credits datasets using the movie title.

### 2. Data Preprocessing

- Select relevant movie attributes.
- Remove rows containing missing values.
- Extract genre names and keywords from structured data.
- Extract the top three cast members.
- Extract the movie director.
- Convert movie overviews into individual words.

### 3. Feature Engineering

Combine the following attributes into a single column called `tags`:

- Overview
- Genres
- Keywords
- Cast
- Director

This combined feature represents the content of each movie and is used for calculating similarities.

### 4. Text Processing (Stemming)

Apply the **Porter Stemmer** from NLTK to reduce words to their root forms.

This helps normalize similar words before converting the text into numerical representations.

### 5. Text Vectorization (Bag of Words)

Use Scikit-learn's `CountVectorizer` to convert movie tags into numerical vectors.

Configuration:

- Maximum features: 5,000
- Stop words: English

### 6. Cosine Similarity

Use Scikit-learn's `cosine_similarity` to calculate the similarity between movie vectors.

Movies with higher cosine similarity scores are considered more similar in terms of their content.

### 7. Movie Recommendations

The `recommend()` function:

- Takes a movie title as input.
- Finds its corresponding index.
- Retrieves similarity scores.
- Sorts movies based on similarity.
- Displays the top five similar movies.

## 🚀 Installation & Usage

### Prerequisites

- Python 3.x
- pip
- Internet connection for downloading the dataset

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/movie-recommendation-system.git
```

Navigate to the project directory:

```bash
cd movie-recommendation-system
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Project

If using the Python script:

```bash
python movie_recommender.py
```

If using Google Colab or Jupyter Notebook, open `movie_recommender.ipynb` and execute the cells sequentially.

### 4. Generate Recommendations

At the end of the project, call the recommendation function with a movie title:

```python
recommend('Fight Club')
```

The system will display five recommended movies based on content similarity.

## 📚 Concepts Learned

Through this project, I practiced and gained hands-on experience with:

- Data collection and exploration
- Data cleaning and preprocessing
- Feature engineering
- Natural Language Processing (NLP)
- Text preprocessing and stemming
- Bag of Words (BoW)
- Text vectorization
- Cosine Similarity
- Content-Based Recommendation Systems

## 🎯 Project Objective

The main objective of this project was to understand how recommendation systems work and gain practical experience implementing a content-based recommendation approach using Python and NLP techniques.

This project is part of my ongoing Machine Learning learning journey.

## Asfandyar Khan

Aspiring AI Engineer | Machine Learning Enthusiast

---

⭐ If you find this project useful, feel free to explore the repository and share your feedback.

