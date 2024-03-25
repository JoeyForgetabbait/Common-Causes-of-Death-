# Common-Causes-of-Death-
Analyze common causes of death internationally and develop conclusions. 



# Top 5 and bottom 5 Causes of Death Analysis
Using the data from the merged data set of cause_aid_pop_df we performed a sum() fucntion acroos the columns that were causes of death from 1990-2019. This created a new df that had the total amount of deaths caused by each specific disease. We then sorted them by using the sort_values function which gave us the a list fo the causes of deathn from the most deadly to the least deadly. To just take the top 5 and bottom 5 we filtered the df to only give the first 5 and the last 5. These two new dfs were then plotted as a pie chart and a bar graph to visualize the top and bottom 5 casues of death from the period of 1990-2019.

# Normalizing the Data to Show Death per Capita 
We wanted to normalize the data based on population so that wecould compare them not just soley on raw numbers. To do this a causes_pop_df was created by merging the population to the causes of death csv. To get this desired df we had to iterate through the causes_pop_df and divide each death count of each year in each country by the countrys specific population then add that calculated value to a new columns of the df. Once this was completed the new df was filtered to only include per capita data and the population of each country during the specified year. Once this new df was created a fucntion was also created so that a specific country code could be plugged in and the fucntion would return a df that had the top 5 causes of death in that country over the 30 year period(1990-2019). A similar function was also created that would return the bottom 5 causes of death for a specifc country code over the 30 year period. This fucntion made it very easy to create different visualition based on death per capita for a specific country. 

# Geographical Anaylsis
Using the information from Google's coordinate spreadsheet (countries.csv), we created a new data frame "country_totals" to group the data by country and sum up the 30 year data from our existing "cause_aid_pop_df" dataframe. We iterated through the values in the "Country/Territory" column of country_totals dataframe and checked if the country name exists in the "name" column of the google spreadsheet. If there is a match, it will retrieve the latitude and longitude columns from the Google spreadsheet and add it to the "country_totals" dataframe. The final results are exported to "results.csv" in the resources folder.
Now that every country in our dataframe has coordinate data, we implemented two hvplots to map the total malaria deaths and total aid given per country over the 30 year span. The scaling was adjusted so that each point was legible on the map. The stats are also viewable when you hover over each point.
