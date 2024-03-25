# Common-Causes-of-Death-
Analyze common causes of death internationally and develop conclusions. 

# Geographical Anaylsis
Using the information from Google's coordinate spreadsheet (countries.csv), we created a new data frame "country_totals" to group the data by country and sum up the 30 year data from our existing "cause_aid_pop_df" dataframe. We iterated through the values in the "Country/Territory" column of country_totals dataframe and checked if the country name exists in the "name" column of the google spreadsheet. If there is a match, it will retrieve the latitude and longitude columns from the Google spreadsheet and add it to the "country_totals" dataframe. The final results are exported to "results.csv" in the resources folder.
Now that every country in our dataframe has coordinate data, we implemented two hvplots to map the total malaria deaths and total aid given per country over the 30 year span. The scaling was adjusted so that each point was legible on the map. The stats are also viewable when you hover over each point.

# Checking whether foreign aid receiving affects causes of death
* Here we are creating dataframes for High aid receving contries and Low aid receving contries with top and bottom death causes.

* First,we started with top causes of death in high and low aid receving countries,so that, 'Current Amount of Aid Given by US ($USD)' column in the main dataframe 'cause_aid_pop_df' is sorted in the descending order and found the highest aid receving countries.

* Created a dataframe using the top aid receving countries and top causes of death as 'filter_top_df'.

* Filtered this data frame with years.

* Lastly performed  grouped by 'Year' function on this dataframe with mean as the aggregation function and got the average top cusess of  death in high aid receving countries over year dataframe as 'top_aid_df'.

* The same logic applied in finding the average death in low aid receving countries over year by sorting the 'Current Amount of Aid Given by US ($USD)' colomn in acsending order and got the dataframe as 'bottom_aid_df'.

* Visualized both 'top_aid_df' and 'bottom_aid_df' using line plot.

* The above steps are repeated for creating average least causes of death in high and low aid receving countries over yers by using the bottom_causes.

* The main conclusions are as follows:

1-High Aid Receiving Countries: the data suggests that US aid efforts had a non-trivial, positive impact on causes of death arising from public health-related factors  (respiratory infections and diarrheal disorders).


2-Low Aid Receiving Countries: the data suggests that the reduction/elimination of US aid had a tremendous impact from 2000 - 2019.

# Finding percentage of deaths in high and low income countries.
* First find the percentage of death of deaths in different countries over year as 'Cause_aid_pct_df'

* Grouped the dataframe by 'Country Income Category' column and named the dataframe as 'income_death_pct_df'

*  Performed transpose function on the 'income_death_pct_df' dataframe to get the income catogory as columns.

* plotted two bar graphs,one with y axis as 'High Income Country' for finding "Percetage death in High income countries" and the other with y axis as 'Low Income Country' for finding "Percetage death in Low income countries".

* The main conclusions from the visualization are:
1-  Cardiovascular diseases and neoplasms are a worldwide problem.
2- Deaths that can be attributable in large part to public health conditions (diarrheal, respiratory) are twice as high in low income countries than they are in high income countries.
