## Movie Recommendation System

### Overview
This Python script implements a movie recommendation system based on movie plots and other attributes. It utilizes techniques such as CountVectorizer, TF-IDF Vectorizer, and Cosine Similarity to recommend movies similar to a given movie title.

### Prerequisites
- Python 3.x
- pandas
- scipy
- scikit-learn

### How to Use
1. **Import Required Libraries**: Ensure you have installed the necessary libraries by running `pip install pandas scipy scikit-learn`.

2. **Prepare Dataset**: Place your movie dataset in a CSV file named `dataset.csv`. The dataset should include columns for `movie_id`, `original_title`, `cast`, `genres`, and `plot`.

3. **Run the Script**: Execute the script `movie_recommendation.py` after setting up the dataset and required libraries.

4. **Input**: Provide the name of a movie for which you want recommendations.

5. **Output**: Receive a list of recommended movies based on similarity to the input movie.

### Explanation of Functions
- `get_data()`: Loads the movie dataset from the CSV file and preprocesses it.
- `combine_data(data)`: Combines relevant columns of the dataset to create a unified feature set for recommendation.
- `transform_data(data_combine, data_plot)`: Transforms the combined data using CountVectorizer and TF-IDF Vectorizer and computes cosine similarity between movies.
- `recommend_movies(title, data, combine, transform)`: Recommends similar movies based on the input movie title.
- `main(movie_name)`: Main function to execute the recommendation process.

### Example
```python
recommendations = main("Inception")
print(recommendations)
```

### Note
- Ensure the movie titles provided as input are consistent with the titles in the dataset to receive accurate recommendations.
- Experiment with different parameters and techniques to improve recommendation quality.
