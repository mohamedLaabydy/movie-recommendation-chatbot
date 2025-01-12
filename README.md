# Movie Recommendation Chatbot 🎥🤖

## Introduction
This project focuses on building a chatbot that recommends movies based on the user's mood and engages in discussions about movies. By leveraging a pre-trained language model, the chatbot provides personalized recommendations and movie insights, creating an interactive and enjoyable user experience.

## Objective
Recommend movies tailored to the user's mood.
Discuss movies by providing information like synopsis, genre, release year, and similar recommendations.

## Key Features
### Mood-Based Recommendations
Suggests movies based on the user's current mood (e.g., happy, sad, adventurous, romantic, scared).
Utilizes a predefined dataset of movies to map user moods to corresponding genres.

### Movie Discussions
Shares details about specific movies:
Synopsis
Genre
Release Year
Recommendations for similar movies

## Dataset
1- The project uses the Movies Dataset available on Kaggle. Steps to prepare the dataset:
The dataset is downloaded using KaggleHub:
```python
import kagglehub
path = kagglehub.dataset_download("akshaydattatraykhare/movies-dataset")
print("Path to dataset files:", path)
```
2- Data preprocessing includes:
Removing unnecessary columns like budget, homepage, production_companies, etc.
Filtering movies with less than 50 votes.
Keeping only movies with a vote average greater than 8.2 to reduce model complexity.


## How It Works 
1- Dataset Preparation:

Data is formatted into a context string containing movie titles and overviews.
Unnecessary entries are removed, ensuring high-quality data input.

2- Chatbot Design:
The chatbot leverages the tiiuae/falcon-7b-instruct model for generating human-like responses.
The context (movie dataset) is fed into the model to enable relevant movie recommendations and discussions.

3- Interactive Queries:
Users can ask the chatbot for:
Movie recommendations based on specific moods or themes.
Detailed insights about a particular movie, including its story and moral lesson.


## Results 
 User Interaction: The chatbot engages users in movie-related conversations and provides tailored recommendations.
 Mission Accomplished: The chatbot is a movie-savvy companion, ready to enhance your movie nights! 🎬🍿


## Feature Improvements 
Expand the dataset to include more movies for diverse recommendations.
Integrate an interactive user interface (e.g., using Flask or Streamlit).
Incorporate user profiles for personalized recommendations.
