# Merging data

Data from nflsavant.com didn't have a unique key. I audibled and chose to
get data from the people who developed nflscrapR (https://github.com/ryurko/nflscrapR-data/tree/master/play_by_play_data).
The play-by-play data has a unique key "GameId" which seems to be scraped from NFL.com.
For example, one of the unique id's "2014011901" is the 2014-01-19 game between SF and SEA.
The Game Id can be found within the below URL
(https://www.nfl.com/gamecenter/2014011901/2013/PRO20/49ers@seahawks).

The Weather data ant scraped has a unique composite key game_id that is in the following format: gamedate + 0 + hometeam.
Ant created a mapping to convert home teams to the url formatting in the pbp dataset and transformed the original game_id key to
match the weather dataset. This allowed for a successful join.

The merged dataset contains 212,142 rows and 275 columns. We will need to do some sort of dimensionality reduction for this
dataset to be workable.



