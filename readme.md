# Song Recommender
***

## Table of Contents
1. [Project Overview](#project-overview)
2. [Prerequisites](#prerequisites)
3. [Setup](#setup)
4. [Functionality](#functionality)
5. [Note](#note)
10. [Contributors](#contributors)


## Project Overview
This Python project utilizes the Spotify API and machine learning techniques to recommend songs based on user input. The recommendation system incorporates both a list of top songs and a clustering model to provide diverse and personalized suggestions.

## Prerequisites
Ensure you have the following libraries installed:

```bash
pip install pandas regex spotipy scikit-learn
```

## Setup
1. Clone the repository:
```bash
git clone https://github.com/laiagomezmessia/lab-web-scraping-single-page.git
```

2. Create a Spotify Developer account and obtain your client ID and client secret.
   
3. Create a file named secrets.txt in the project root:
```bash
clientid: YOUR_CLIENT_ID
clientsecret: YOUR_CLIENT_SECRET
```

4. Ensure you have the following CSV files in the project directory:
top_songs.csv: List of top songs.
playlist_df.csv: Playlist with relevant features.

5. Run the recommend_song function in SongRecommender.ipynb:
```bash
python song_recommender.py
```
Enter a song and its artist when prompted to receive a song recommendation.


## Functionality
The recommend_song function performs the following steps:

1. Checks if the user-inputted song is in the top songs list. If yes, it recommends a random song from the remaining top songs.

2. If the user-inputted song is not in the top songs list, it connects to the Spotify API, searches for the song, and retrieves its audio features.

3. Uses a pre-trained KMeans clustering model to predict the cluster of the input song.

4. Recommends a random song from the same cluster in the playlist DataFrame.

5. Introduces a nap to avoid hitting rate limits when interacting with the Spotify API.


## Note
- The clustering model and scaler are loaded using pickle from files named kmean.pkl and scaler.pkl. Ensure these files are present in the project directory.

- The script can be further extended to include additional features or improve the recommendation algorithm.

Feel free to explore, modify, and enhance the project according to your preferences!


## Contributors
- [Laia Gómez Messía](https://github.com/laiagomezmessia)
