# Movie Recommendation System

This project implements a movie recommendation system using a dataset of movies and their associated information. The system utilizes the cosine similarity between movie tags to provide recommendations for similar movies based on user input.

## Dataset

The project uses two datasets:

1. `tmdb_5000_movies.csv`: This dataset contains information about various movies, including their title, overview, genres, keywords, cast, crew, and other details.

2. `tmdb_5000_credits.csv`: This dataset provides information about the credits for each movie, including the cast and crew details.

## Data Preprocessing

The code performs several preprocessing steps to prepare the data for the recommendation system:

1. **Merging Datasets**: The code merges the `movies` and `credits` dataframes based on the movie title.

2. **Selecting Required Columns**: The code selects the required columns for the recommendation model, including `movie_id`, `title`, `overview`, `genres`, `keywords`, `cast`, and `crew`.

3. **Handling Missing Values**: The code checks for null values and drops any rows with missing values from the `movies` dataframe.

4. **Handling Duplicates**: The code checks for duplicate entries in the `movies` dataframe and removes any duplicates.

5. **Formatting Genres, Keywords, Cast, and Crew**: The code formats the genre, keyword, cast, and crew sections by extracting the relevant names and storing them as lists.

6. **Splitting Overview Section**: The code splits the overview section of each movie into a list of words.

7. **Removing White Spaces**: The code removes white spaces between words in the genres, keywords, cast, and crew sections.

8. **Creating Tags Column**: The code creates a new column called 'tags' by merging the overview, genres, keywords, cast, and crew sections.

9. **Creating New Dataframe**: The code creates a new dataframe (`new_df`) containing the `movie_id`, `title`, and `tags` columns.

10. **Converting Tags to String**: The code converts the tags from a list to a string format.

11. **Lowercasing Tags**: The code converts the tags to lowercase for consistency.

## Movie Recommendation

The recommendation system is implemented using the cosine similarity between the movie tags. The steps involved are as follows:

1. **Vectorization**: The code uses the `CountVectorizer` from the scikit-learn library to convert the tags into numerical vectors. It sets a maximum number of features to 5000 and removes common English stop words.

2. **Calculating Cosine Similarity**: The code calculates the cosine similarity between the vectors obtained from the tag vectorization.

3. **Recommendation Function**: The code defines a `recommend()` function that takes a movie title as input and returns the top 5 similar movies based on the cosine similarity scores. It prints the titles of the recommended movies.

4. **Example Usage**: The code provides an example usage of the `recommend()` function by recommending similar movies to the movie "Inception".

## Dependencies

The code requires the following dependencies:

- numpy
- pandas
- ast
- sklearn

Make sure these dependencies are installed before running the code.

## Running the Code

To run the code, perform the following steps:

1. Ensure that the required datasets (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) are present in the same directory as the script.

2. Install the required dependencies mentioned above.

3. Execute the script, and it will display the recommended movies for the given example usage.

Feel free to modify the code or dataset to experiment with different movies and recommendations.

Enjoy using the Movie Recommendation System!
