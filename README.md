# Book_Recommendation_System
This project implements a hybrid recommendation engine that combines Global Popularity and Personalized Collaborative Filtering to provide optimized book suggestions.

# 1. Popularity-Based Recommender
Designed to solve the "Cold Start" problem, this tier recommends books to new users who have no prior rating history.

*Selection Logic:* Identifies books based on a weighted average rating.

*Filtering:* Only books with more than 250 ratings are considered to ensure suggestions are based on a significant consensus rather than a few outliers.

*Outcome:* Provides a Top 50 trending list of globally acclaimed titles.

# 2. Collaborative Filtering System
This tier delivers deep personalization by analyzing behavior patterns across a filtered community of "Power Users."

*Data Sculpting:* The dataset is refined to include only users who have rated >200 books and titles with >50 ratings, significantly reducing noise.

*Matrix Transformation:* Data is structured into a pivot table (User-Item matrix) where missing values are handled to create a dense vector space.

*Similarity Metric:* Uses Cosine Similarity to calculate the distance between book vectors. This identifies books that share similar "rating patterns" regardless of the absolute number of votes.

# 3. Technical Implementation
*Functionality:* The system includes a recommend() function that takes a book title, finds its position in the high-dimensional vector space, and retrieves the Top 5 nearest neighbors.

*Tech Stack:* Python, Pandas, NumPy, and Scikit-learn.
