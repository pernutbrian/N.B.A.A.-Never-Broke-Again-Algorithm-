# N.B.A.A.-Never-Broke-Again-Algorithm-
Neural network built w/ Tensorflow that aims to predict NBA games for the purpose of sports betting. (Work In Progress, tips and recommendations welcome.)

Data is pulled from https://pypi.org/project/nba-api/

To do

-add the file that pulls seasonal data (makes a csv file of a whole season and then stacks them together.)

-add a check to see if teams inputted are the same. MIA vs. MIA is invalid

-possible something has been overlooked. my stats holding data structures dont reset season to season. Meaning that the 1st season holds the data from season 1, season 2 from 1 and 2, and season 3 from 1,2,and 3. No way of knowing yet if this helped my model in the end but it would reward teams that did good during that period. If I did that the last 30 years instead where the average stats may be more similar, this would make my model do worse. Have to check model with stats resetting and with less seasons(currently at 5)
                           
-~v.0.3 must be a redone version. need to use some NBA api directly so all of my data could be extracted from one row instead of the current 2 rows of data. This would simplify ExtractData(), and make NBAA easier to update. We are struggling right now.~ done. ExtractData is now indeed easier to read

-found that in my dictionary i had both toronto and utah with the same number. major error.

-v0.4 will include a version that predicts the money line instead of win/loss. if its not too big of an update it will become 0.3.1

-v0.5 will include a version that predicts money line and winner after the stats of the first, second, third quarters to do live betting. This one should shuffle the games. This one is finding live trends in a game, not live trends over a season
