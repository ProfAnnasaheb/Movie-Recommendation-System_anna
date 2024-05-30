This movie recommendation system uses metadata from a dataset to recommend movies based on a user's favorite movie. The system combines several features of each movie, including genre, keywords, tagline, cast, and director, to calculate similarity scores and provide recommendations.

Steps Involved:
Data Loading:

The movie metadata is loaded from a CSV file using pandas.
Feature Extraction:

Selected features (Movie_Genre, Movie_Keywords, Movie_Tagline, Movie_Cast, Movie_Director) are combined into a single text string for each movie.
Missing values in these features are filled with an empty string to ensure consistency.
Text Vectorization:

The combined text strings are transformed into numerical representations using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization.
This helps in converting the textual information into a form that can be used for similarity calculations.
Similarity Calculation:

Cosine similarity is used to compute similarity scores between the user's favorite movie and all other movies in the dataset.
The cosine similarity metric measures the cosine of the angle between two non-zero vectors, which in this case represent movies.
User Input Handling:

The system takes the user's favorite movie name as input.
It validates the input by finding the closest match to the provided movie name using the difflib library.
Recommendation Generation:

Based on the similarity scores, the system sorts the movies in descending order of similarity.
It then outputs the top 30 recommended movies to the user.
