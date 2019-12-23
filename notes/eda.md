# Initial exploration

We decided to look at the play by play data from nflsavant.com first in order
to see what we had readily available. It turns out a lot of the data that is
on there is really useful - we can easily tell whether a play is a pass or a
rush, as well as surrounding information about the play.

We also have a lot of NAs in several columns, as well as some empty columns.
There's also a few columns that only have one constant value, and some columns
that are binary. The NA examination is yet to be done.

Looking at the distribution across downs, it was also apparent that pass/rush
distributions are different depending on which down a play is on.

Since we had just been looking at 2019 data, we also had to examine the merged
dataset from 2013-2019 - all of the data from nflsavant. Merging the data was
pretty easy, though reading some of the files in was annoying since the csv
does not escape quote characters in the standard way, but rather using an
escape character of `\`. Once this was dealt with, the data showed nearly
identical distributions as 2019 for pass/rush by down.

Once we looked at weather data, we established that we only have weather data
up until 2013, whereas the play by play data is from 2013 on. This means we
don't actually have any relevant weather data. One avenue that we can explore
is scraping the weather information for our games from ProFootballReference.com
.

