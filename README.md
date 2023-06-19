## Movie Recommendation System

This project implements a movie recommendation system using the TMDB 5000 Movies dataset. The system utilizes natural language processing techniques to analyze movie descriptions, genres, keywords, cast, and crew information to provide personalized recommendations.

### Requirements
- Python 3.x
- numpy
- pandas
- scikit-learn

### Dataset
The dataset used for this project consists of two CSV files: `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`. These files contain information about movies, including titles, overviews, genres, keywords, cast, and crew.

### Project Overview
1. Read the movie and credits datasets using pandas.
2. Merge the credits dataframe into the movies dataframe based on the movie title.
3. Select the required columns for the model.
4. Check for null values and drop missing values.
5. Format the genres, keywords, cast, and crew sections by extracting relevant information.
6. Split the overview section into a list of words.
7. Remove white spaces between words in the genres, keywords, cast, and crew sections.
8. Create a 'tags' column to merge the overview, genres, keywords, cast, and crew sections.
9. Create a new dataframe with movie_id, title, and tags columns.
10. Convert tags from a list to a string and convert it to lowercase.
11. Vectorize the tags into numerical vectors using the CountVectorizer.
12. Calculate the cosine similarity between the vectors.
13. Implement a recommend function to fetch similar movies based on a given movie.
14. Example usage: recommend('Inception')

### Usage
1. Ensure that the required libraries are installed.
2. Download the `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` files.
3. Run the code and explore movie recommendations.

Feel free to customize and modify the code to suit your needs. Enjoy exploring movie recommendations!
