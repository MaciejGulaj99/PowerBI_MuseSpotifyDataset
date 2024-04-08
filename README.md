# Muse Spotify Dashboard - overview


## About
This project is quite simple Muse's songs and albums popularity overview on Spotify. We can dive in into Spotify various descriptive variables like Valence, Danceability or Popularity to ranking all songs and albums. Thanks to them we can know which are the most favourite by Spotify listeners. Dashboard was created in PowerBI. It contains:
* custom DAX calculations with variables
* custom tooltips
* custom background created in PowerPoint



## Source

Original dateset comes from Kaggle repository owned by Tim Buck - https://www.kaggle.com/datasets/timbuck/muse-album-songs-data-from-spotify.
Data was collected on 14/12/2022 and includes all Muse songs that feature on albums starting from Showbiz (1999) to Will of the People (2022).


## Analitycal Questions

I used ideas for simple analitycal tasks Tim's repository. There are all described below:

1. Which album has the longest songs?
2. Has the mood of songs gotten happier, sadder, or remained the same throughout Muse's career?
3. Is there any correlation between popularity and key, energy or danceability?


## Analysis

Let's try answer this questions.
1. First of all, we should create some measures and charts. Task looks quite simple, so we can limit ourselves to basic stuff. We will need average song duration (in original dataset we have miliseconds, i converted to seconds) and 'album-name' to build vertical and horizontal Bar Charts and Matrix with descending sorting.

![obraz](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/06675cda-3340-4af1-8172-f30e1e281e37)

We can notice that the longest songs on album are in concert album called "HAARP" with 308 seconds (5:08) on average.


## Dashboard

1. Tooltips overview on 'General Info' page

![gif-muse1](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/babab9c0-c813-4779-96a2-4abbd787bd97)
