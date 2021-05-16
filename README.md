# anime-recommendor
Recommend Anime using Alternating Least-Squares algorithm and more

This is a repo for distributing a part of a Anime recommender project I'm involved in.

This is currently a work in progress. We're expecting to add more recommendation algorithms for better performance.

This project provides
- A fully functional MySQL database manager that can store and speedily retrieve user/anime rating data
- An ALS algorithm that supports numpy batch computing

TODO
- Test ALS algorithm
- Make ALS training distributed
- Add more recommendation algorithms

Data
We retrieved data from [MyAnimeLists Kaggle dataset](https://www.kaggle.com/azathoth42/myanimelist).

Trying out

Download
- UserList.csv
- anime_cleaned.csv
- animelists_cleaned.csv

from MyAnimeLists Kaggle Dataset.

UserList is csv file for the users table in sql database
anime_cleaned.csv is csv file for the animes table in sql database
animelists_cleaned.csv is csv file for ratings table in sql database

run convertCsvToDataFormat.py to create a MySQL friendly ratings csv file, which replaces user names and anime ids with primary keys.

In alsDatabaseManager.py, run createUserAnimeDatabase() and completeInitialize(...) with the necessary parameters.

In ALSTrainer.py, run ALSTrain.
