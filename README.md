**INTERIM REPORT**

Our project is about the Eurovision Song Contest, the patterns in Eurovision voting, an examination of the genre trends
and an analysis of the performances in order to create a winner prediction model.

We already had a dataset which had all the points given from one country to another from 1975 to 2019 which we'll use to
work on the first problem we want to tackle (voting patterns) but we had to analyze other data on our own for the other two 
problems.


**New datasets**

We've researched and created two new datasets which will help us better analyze and understand the Eurovision Song Contest.

The first one is a dataset with all the performances in the final from 2015 to 2019 categorized. The categories used to describe
each contestant are the following:

1. year<br>
2. country<br>
3. name of performer<br>
4. song title<br>
5. solo, duo or group<br>
6. song genre<br>
7. song rating<br>
8. performance rating<br>
9. alone on stage<br>
10. special effects<br>
11. props on stage<br>
12. memorability rating<br>
13. choreography<br>
14. backup dancers<br>
15. final placement<br>
16. televoting<br>
17. jury<br>
18. total<br>

Category number five is about the performer, whether they're solo or else.<br>
The category "song genre" can have the following values: 
sentimental ballad, power ballad, dance pop, ethnic, pop rock, 
popera (operatic pop), country, pop ballad, pop, electro (electronic), outlier and debatable.

The song, performance and memorability rating categories are mostly subjective based on our opinion, 
and they include integer values from 1 (bad) to 5 (great). Memorability rating is greater when the performance is 
controversial or unusual, or just well made and beloved by the Eurovision audience.

The categories alone on stage, special effects, props on stage, choreography and backup dancers aim to describe the performance. 
Their values are either "yes" or "no". Alone on stage is "no" even if the only other people on stage are backup vocals, 
props on stage being "yes" could mean anything from instruments to coffins, suitcases etc. being part of the performance. 
Special effects mostly means that the artists included pyrotechnics, special visual effects that alter the performance 
(not including the animated screen behind the performer which is present for every performance) or else. 
Each performance has a choreography, however, the performance will only be described as having a choreography if it's elaborate, 
the dance moves are cautiously planned etc. 

Televoting and jury points aren't available for 2015, but they are for the years 2016-2019. 
Each country votes twice, once by televoting (anyone from the country can vote) and once via specialized jury 
(critics specifically chosen by that country). When combined, we get the total points the country won that year. 
Jury and televoting opinion always differs, sometimes more drastically, sometimes less. 
With this dataset, we can see how their tastes differ. 

*Most popular and prevalent genres*

Out of the 12 genres, pop is the most popular one.

![Genres histogram](https://github.com/AP2166/PR20APMDKC/blob/master/genres.jpg)

Eurovision song genres aren't always strictly defined and most songs have multiple genres, or belong to a specific subgenre.
Whether we analyze them by their main genre or their specific subgenre, pop is the predominant genre 
with almost 50% of the songs belonging to this genre, and the second place belongs to the electronic genre. 
Ballads are also very popular, as well as ethnic songs. Rock and country are the least popular genres.

The "outlier" and "debatable" categories include songs with gospel, funk, swing, industrial techno elements etc.

*Performances*

We analyzed the atributes we had to describe the performances and we got the following results:
The usual Eurovision performer is a solo artist who isn't alone on stage, has special effects in their performance, 
has props on stage, doesn't have an elaborate choreography and doesn't have backup dancers.

Almost half of the artists who end up in the top 5 are alone on stage and don't have an elaborate choreography, 
they predominantly have special effects on stage, it's slightly more likely that they don't have backup dancers.

![Winners](https://github.com/AP2166/PR20APMDKC/blob/master/winners.jpg)

When it comes to winning performances, the variables aren't that equally distributed.
A winning performance from 2015 to 2019 usually means the artist is alone on stage, doesn't have special effects or props 
on stage, dancers are rarely included and an elaborate choreography is also rare. 
Their performances are usually memorable and well rated, with a good song. The only exception in this list is 
last year's winner, whose song and performance were mediocre, but the compromise between jury and televoting led to its victory.

The trends of this decade are very different from the trends of last decade. From the years 2001 to 2009, 
all the winners weren't alone on stage and the predominant type of winning performance was flashy, well choreographed 
and overall very energized.
From 2010 to 2019 however, the accent is put on the individual artist's stage presence and their ability to engage the audience. 
Only three winners out of ten weren't alone on stage (Azerbaijan 2011, Denmark 2013 and Israel 2018).

In 2015, the most popular genre was power ballad which makes sense, since the 2014 winner was quite a memorable power ballad 
(Rise like a Phoenix by Konchita Wurst).
In 2016 and 2017, the most popular genre was pop, the winner in 2015 was a dance pop song. 
The winner in 2016 had mixed ethnic and pop elements.
The most popular genre in 2018 and 2019 was dance pop.

We can see that the winning genres in the past few years are quite diverse.

*Differences between jury and televoting points*

Statistics of the televoting points versus the jury points:<br>
std               92.772198                     78.694959<br>
min               -1.000000                     -1.000000<br>
25%                3.000000                      9.000000<br>
50%               35.000000                     48.000000<br>
75%              102.500000                    114.500000<br>
max              376.000000                    382.000000<br>

By analyzing the top five contestants according to the jury and televoters from 2016 to 2019 (2015 didn't have the split voting
system), we can see that the only year when the jury and the televoters agreed was 2017, when they both chose Portugal as the
winner and Bulgaria as the runner-up.
In 2019, there are vast disparities between the jury and televoting points awarded to North Macedonia (winner according 
to the jury, difference of 189 points), Norway (televoting winner, difference of 251 points) and Sweden (second according 
to the jury, difference of 148 points).
The winner and the runner-up (Netherlands and Italy) have much smaller deviations in points. 
In 2018, only two countries appear on both of the lists of the top five by jury and televoting points, 
Israel (who was the winner, also was the winner according to televoting but third according to the jury) and 
Cyprus (who was second according to televoting and second in total, was fifth according to the jury).
In 2016, once again the jury and the televoters disagreed. They both agreed that Ukraine should be the runner-up 
(however, Ukraine ended up being the winner), but the jury picked Australia for the winner (Australia ended up being 
the runner-up), while televoters picked Russia as the winner (Russia ended up third).
Here we can also see some discrepancies between the votes, notably Poland (215 points difference), 
Russia (231 points difference), Australia (129 points difference) and Malta (113 points difference).

This analysis isn't finished, since our goal is to find which categories matter more when it comes to winning or better placement.
For data analysis, we used the pandas and matplotlib libraries.

*Link to the Jupyter notebook:*
https://github.com/AP2166/PR20APMDKC/blob/master/Performance%20analysis.ipynb

*Link to the dataset:*
https://github.com/AP2166/PR20APMDKC/blob/master/2015-2019%20performers.xlsx



The second dataset is focused on exploring the genre trends by country from the beginning of the Eurovision Song Contest to the present day. The column values are all the countries that have participated, and the row values are years, from 1956 to 2019.
We organized the genres into ten possible categories:<br>
sentimental ballad, power ballad, upbeat pop, dance pop, ethnic, (pop) rock, popera, country, outlier and debatable.

We also separated the winners in a different dataset so we could analyze the winning trends.

![Genre distribution](https://github.com/AP2166/PR20APMDKC/blob/master/genre_distribution.jpg)

Here we can once again see that pop is the most popular genre, specifically dance pop, closely followed by sentimental and power
ballads. 

![Winning vs prevalent](https://github.com/AP2166/PR20APMDKC/blob/master/winning_vs_most_prevalent.jpg)

We wanted to see whether the most present genre of the year is also the winning one. 
As we can see, this is not usually the case.

![Winning countries throughout the years](https://github.com/AP2166/PR20APMDKC/blob/master/win_countries.jpg)

Here we can see all the winning countries. Ireland is the country with the most wins, the only country to win with the same
performer twice, and the only country to win three years in a row. They've also won with 4 different genres from our genre
categories.

