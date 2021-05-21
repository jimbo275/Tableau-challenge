
# Citibike data analysis

**Goal of our Analysis** 
Our report aims to find the impacts of COVID 19 on ridership among Jersey City Citibike riders and evaluate the impact on common rider metrics.

**Data Description** 
As part of our analysis of Citibike data, we examined monthly ridership in Jersey City (JC) through the period 1/1/2019 through 4/30/2021. The data is comprised of a number of monthly files containing the following columns: 
-Trip duration (seconds) 
-Start Time 
-Stop Time 
-Start Station ID 
-Start Station Name 
-Start Station Latitude 
-Start Station Longitude 
-End Station ID 
-End Station Name 
-End Station Latitude 
-End Station Longitude 
-Bike ID 
-User Type (Subscriber or Customer) 
-Birth Year 
-Gender (0 = Male, 1 = Female, 2 = Not provided)

**Data Scrubbing** 
We imported the data into Python and using the Pandas and geoPy libraries, concatenated the CSV data files into a single large Output file. Using geoPy, we computed the distance in miles between the starting and ending station points. We also removed outliers (e.g. riders with ages above 95 - while not completely out of the ordinary, it would be unlikely for them to be customers). We also compiled a list of the top and bottom stations by ride count and generated a table of top and bottom destination stations. In addition, we converted time duration (in seconds) into hours and used the data-of-birth information to compute rider ages.

**Business Questions** 
Our visual analysis of the data comprised a number of graphs and dashboards, designed to answer a number of questions about Citibike riders. Namely:
•	What is the breakdown between customer and subscription riders by trip count and how has this changed over time?
•	What are the top and bottom 10 destinations?
•	How has the split between male and female riders changed over time?
•	What is the average distance a bike is ridden?
•	How many trips were recorded during the chosen period?

**Findings** 
Our findings could be divided into a number of themes, explained in detail below.
*Ridership* 
Of the approximate 800K rides over the period Jan 2019 - Dec 2020, between 20-25% were female, 65-75% were male and 3-22% were "not provided". These ratios changed dramatically in the early months of 2021 with much larger numbers of "Not provided" riders (75-95%) as dramatically smaller ridership numbers were posted. This may be due to a data issue or perhaps a change to the app. Even though the ratio of male riders to "Not provided" changed substantically during the 2020 Covid pandemic, the number of female riders increased slightly over 2019, leading us to conclude there may be some issue with the app or the data itself.

*Top Start/Stop locations* 
The top starting stations during the period are typical of commuter traffic, with Grove St. PATH, Newport PATH and Liberty Light Rail among the top 10. Other locations are closer to the water. A similar list of stations is for ending stations, indicating round trips. The lowest traffic stations are in Manhattan, possibly due to a handful of riders abandoning their rides on the other side of the river. Although riders declined over 2020, the most/least popular destinations did not change.

*Average bike distance* 
Female riders tended to skew younger, with an average age of about 35, while male riders were about 40 years old. The vast majority of rides averaged less than a mile. Presumably few riders want to pay the extra $0.12/minute for rides over 45 minutes. A few outliers here and there (some bikes as high as 8-9 miles) may be bad data, or could simply be the most popular bikes with a die-hard ridership. Of note are the "not provided" riders, who had a average age of about 52. Again, this may be due to a quirk in the ridership app or more people choosing not to provide their ages for other reasons. Distances don't appear to have been much impacted from 2019-2020. Presumably, if riders are choosing to ride, they will get their money's worth and ride the full 45 minutes or so.
*Customers* 
The majority of riders in 2019 (80-95%) were subscribers paying a $15/mth fee. The rest were customers paying either single ride fees of $3.50/trip or day passes ($15/day). In the summer months customer ratios increased to 10-15% of rides as the tourist season hit. In 2020 the percentages shifted considerably, with subscriptions falling to 50-70% of rides while customers made up 30-40%. Numbers of rides declined between 30-50% depending on the month vs 2019. Covid fears may have caused many to cancel their subscriptions and opt to stay home and switch to "as-needed" pricing to offset the uncertainty surrounding commuting.
*Timing* 
Average riders tended to ride during commuter hours i.e. 8am or 6pm, with heavier usage during the summer months and even into Sept/Oct as longer periods of light later in the day are prevalent.

**Conclusions** 
Covid 19 impacted ridership by causing rider numbers to fall and subscription/customer counts to change, with more riders choosing to opt for shorter term payment options rather than multi-month subscriptions. Other metrics such as distance travelled, or most/least popular destinations were not impacted due to COVID.

Graphs of our analysis are published here: https://public.tableau.com/profile/james1565#!/vizhome/Tableau_challenge_051421/CitibikeRidership?publish=yes
