PATTERNS IN EUROVISION VOTING AND WINNER PREDICTION MODEL

The Eurovision Song Contest is a massively popular event and its voting history data is openly available. With the help of two already prepared datasets, we want to explore the voting trends and patterns, whether there's positive bias towards neighbors etc.
Since the voting is divided by jury and televoting, we can explore how the opinion of the "masses" differs from the opinion of the expert jury, and if things like diaspora affect the points given.

The two datasets we already have available are the following:

https://www.kaggle.com/c/Eurovision2010/data

The 2010 Kaggle competition is about Forecasting Eurovision Voting and it includes information about the placements of contestants in finals and semi-finals and the points they got, which block (the territory of Europe is divided into blocks) their country belongs to, the name of the song and the contestant, the contestant's gender, whether they're a solo or group act, the language of the song, as well as the bet rate (how possible it was that they would win).
The goal is to build a prediction model that would predict the possibility of a country winning.

https://data.world/datagraver/eurovision-song-contest-scores-1975-2019

This dataset includes data from the entire competition, from 1975 to 2019, and it shows how many points were given to each country from each country. From this dataset we can analyse the trends, patterns and politics of Eurovision voting.

However, since the Eurovision winners can't be explained by simple politics and whether the song is in English or the contestant's native language, or whether their performance was in a neighbor country or not, we will need more data. 
We want to examine how things like the genre of the song, how popular the song is prior to the competition, stage performance, the contestant's appearance and background and similar politics affect the song's placement.

Examining the entire history of the competition would be too time-consuming, and the type of songs that win have changed, we can analyze the data from the past 5-10 years and see which types of performances had the best placements and which had the worst. 
The song's popularity can be determined from Youtube views and Spotify streams. It's also interesting to see how the jury's choice is often very different from the televoting winner and this results in some interesting compromises. For example, last year (2019) the jury's winner was North Macedonia with 247 points, and the televoting winner was Norway with 291 points, but Norway ended up 6th, North Macedonia got the 7th place, and the Netherlands was the winner.

We will also try to see which genres are popular in which countries and how the tastes of countries and the type of performers they choose to represent them changes over time. 
