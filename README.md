# N.B.A.A.-Never-Broke-Again-Algorithm-
Neural network built w/ Tensorflow that aims to predict NBA games for the purpose of sports betting. (Work In Progress, tips and recommendations welcome.)

Data is pulled from https://pypi.org/project/nba-api/

To do

-~add the file that pulls seasonal data (makes a csv file of a whole season and then stacks them together.)~ added in v.0.3

-add a check to see if teams inputted are the same. MIA vs. MIA is invalid

-~possible something has been overlooked. my stats holding data structures dont reset season to season. Meaning that the 1st season holds the data from season 1, season 2 from 1 and 2, and season 3 from 1,2,and 3. No way of knowing yet if this helped my model in the end but it would reward teams that did good during that period. If I did that the last 30 years instead where the average stats may be more similar, this would make my model do worse.~ fixed in v.0.3 . model prediction increased 6%
                           
-~v.0.3 must be a redone version. need to use some NBA api directly so all of my data could be extracted from one row instead of the current 2 rows of data. This would simplify ExtractData(), and make NBAA easier to update. We are struggling right now.~ done. ExtractData is now indeed easier to read

-~found that in my dictionary i had both toronto and utah with the same number. major error.~ fix done in v.0.3

-v0.4 will include a version that predicts the money line instead of win/loss. if its not too big of an update it will become 0.3.1

-v0.5 will include a version that predicts money line and winner after the stats of the first, second, third quarters to do live betting. This one should shuffle the games. This one is finding live trends in a game, not live trends over a season

-include some form of unit test

-credit the paper that i based mine off from

-made a mistake day 3 with the live betting. need to automate that part to prevent it from happening again

-make a logo of youngboy for the repo (this is just me having fun)

-make last layer have sigmoid. (i think it may already have it as the default but i think relu could be default. specifying removes ambiguity)

~~-combine HT PD and AT PD into one variable to see if it improves the model. hoping that by removing a dimension accuracy improves~~.Dimensionality not always a curse. Change did nothing

-model.fit() has shuffle on by default. this could be hindering my model because my data might give more insight being read sequentially

~~-Training the model on colab has better accuracy than my local machine by 6%. No idea what it could be. Could be the seed or the fact that colab trains off a csv and local off a dataframe. Currently my only ideas but need to figure this out~~ I was right. Turning the dataframe into a CSV and training off that gives my model a 6% difference under the same conditions. This doesnt make any sense to me. I have to open an issue on the tensorflow github as to why a model would train better on CSV values

-wonder if i would have better success rates instead making models for every single team. Would allow me to input games sequentially (use SGD instead), and change one parameter from 1-30 to 1-0 (is the team away or home)
