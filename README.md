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

I used ideas for simple analitycal tasks from Tim's repository. There are all described below:

#### 1. Which album has the longest songs?
#### 2. Have the mood of songs gotten happier, sadder, or remained the same throughout Muse's career?
#### 3. Is there any correlation between popularity and valence, energy or danceability?


## Analysis

Let's try answer this questions.


#### 1. Which album has the longest songs?
First of all, we should create some measures and charts. Task looks quite simple, so we can limit ourselves to basic stuff. We will need average song duration (in original dataset we have miliseconds, i converted to seconds) and 'album-name' to build vertical and horizontal Bar Charts and Matrix with descending sorting.

![obraz](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/06675cda-3340-4af1-8172-f30e1e281e37)

We can notice that the longest songs on album are in concert album called "HAARP" with 308 seconds (5:08) on average.

Below, there is a Treemap Chart using album's theme colors added by field rules. In top-left corner we have Album Name and in bottom-left average song duration. The biggest tile always sits in top-left chart corner.

![obraz](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/430fc5a0-4de1-4399-bc77-281a0bbb0e79)



#### 2. Have the mood of songs gotten happier, sadder, or remained the same throughout Muse's career?

Mood of the songs has been described by "Valence" value. Let's try design line chart with 'album-id' (to be able to sort) on X-axis and 'AverageValence' on Y-axis. For better readability we can add 'album-name' in tooltip. Also, on analitycs page we can add 'Trend line' which give us clearly indicator whether 'valence' going higher or lower. Before that, remeber to sort albums from earliest to latest.

![obraz](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/dbca702c-c8b2-44ea-ae09-210867cc61b6)

So, we can see that trend line is rising which indicates that Muse songs have been happier throughout their career.



#### 3. Is there any correlation between popularity and valence, energy or danceability?

##### Pearson's vs Spearman's Correlation

https://www.statystyka.eu/korelacja-rho-spearmana.php
https://cyrkiel.info/statystyka/wspolczynnik-korelacji-rang-spearmana/

Yes, there is but we should look at this problem from more than one dimension. First of all, let's calculate Pearson's Correlation for all of the songs:

![obraz](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/ec8560c7-4930-48a1-bac6-b4817672706b)

We can see that, there is no correlation between popularity and energy and quite a little between popularity/danceability and popularity/valence. Let's dig in into that.
Take a look on individual albums, which of these have the strongest or the weakeast correlation.

![obraz](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/1ab5881c-551b-4581-aee8-f351d06e6f11)

A quick reminder, how we should interpet our calculate values:

| Pearson correlation coefficient (r) value |	Strength |	Direction |
|-------------------------------------------|----------|------------|
| Greater than .5 | Strong |	Positive |
| Between .3 and .5 | Moderate | Positive |
| Between 0 and .3 | Weak | Positive |
| 0 | None | None |
| Between 0 and –.3 | Weak | Negative |
| Between –.3 and –.5 | Moderate | Negative |
| Less than –.5 | Strong | Negative |

Source: https://www.scribbr.com/statistics/pearson-correlation-coefficient/


## Dashboard

  ### 1. Tooltips overview on 'General Info' page

  ![gif-muse1](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/babab9c0-c813-4779-96a2-4abbd787bd97)


  ### 2. Tooltips overview on 'Correlations' page

  ![gif2](https://github.com/MaciejGulaj99/PowerBI_MuseSpotifyDataset/assets/142632444/87676e9b-a75d-4993-923a-cdaa8bcc0f7a)


  ### 3. Album's filtering


  ### 4. Chart filtering using parameter

