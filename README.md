# Movie Recommendation System

A movie recommendation system designed to provide personalized movie recommendations based on user preferences. This system utilizes collaborative filtering techniques and machine learning algorithms to suggest movies that match users' tastes and preferences. It helps users discover new movies and enhances their overall movie-watching experience.

## Dataset

In our movie recommender system, we use two datasets from Kaggle:
1. TMDB 5000 Movies (Dataset)
2. TMDB 5000 Credits

The movies dataset contains the following columns:
1. Budget
2. Genres
3. Homepage
4. Id
5. Keywords
6. Original language
7. Overview
8. Popularity
9. Production companies

The credits dataset contains the following columns:
1. Movie Id
2. Title
3. Cast
4. Crew

Both datasets contain 5000 records.

## Architecture Diagram

![image](https://github.com/r-an-j-an/Movie-Recommendation-System/assets/100189617/bce666c2-d49d-4992-b496-813bd4b5fa8d)

## Methodology

First, we join the two datasets to get features present in both datasets. The features we are most interested in for our movie recommender are: Keywords, Overview, Genre, Cast, and Crew.

We preprocess the data by converting the 'genre', 'cast', and 'overview' columns into lists containing the required information. From the 'crew' column, we extract and keep only the names of the directors.

Next, we check for the presence of null values in the dataset. As there are only 3 null values out of 5000 records, we choose to omit the records with null values.

Then, we merge the columns we are interested in into one column called 'tags'. This facilitates text vectorization and finding cosine similarities.

Text vectorization is performed based on the frequency of words in the 'tags' column. To find the similarity between two tags, we use cosine similarity measurement.

We accept a movie title from the user, find its relevant data from the dataset, perform cosine similarity with the rest of the movies, and display the most similar results.

![image](https://github.com/r-an-j-an/Movie-Recommendation-System/assets/100189617/f1ea1a95-bb94-48cd-ab4e-5a148b1a7a0d)


## Installation

1. Clone or download all project files to your local machine.
2. Install the necessary dependencies and libraries.
3. Ensure you have the TMDB 5000 Movies and TMDB 5000 Credits datasets available.
4. Follow the instructions in the project code to preprocess the data and perform text vectorization.
5. Run the recommendation system to generate personalized movie recommendations.

## Usage

1. Launch the application by running the recommendation system code.
2. Provide your movie preferences and any available user information.
3. Receive personalized movie recommendations based on your preferences.
4. Explore the recommended movies, view their details, and enjoy discovering new movies tailored to your taste!

## Technologies Used

- Python
- Machine Learning (Collaborative Filtering)
- Pandas
- NumPy
- Cosine Similarity

## Images
![image](https://github.com/r-an-j-an/Movie-Recommendation-System/assets/100189617/c91e0b5e-78cc-4008-bf45-6979a237e885)
![image](https://github.com/r-an-j-an/Movie-Recommendation-System/assets/100189617/07b4d9aa-997b-41fd-8d9a-3048b72f0c6c)



## Conclusion
The Movie Recommender provides real-time suggestion based on the user’s input and preferences.
For the Movie Recommendation System, the Cosine Similarity algorithm has been used to recommend
the best movies that are related to the movie entered by the user based on different factors such as
the genre of the movie, overview, the cast as well as the ratings given to the movie. Although the
system is very accurate, it does have some limitations. One of which is, if the movie entered by the
user isn't present in the dataset or if the user does not enter the name of the movie in the similar
manner as that of in the dataset, then the system fails to recommend movies.
