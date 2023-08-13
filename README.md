# Air-pollution
Air pollution
Q2: Air pollution (30 marks)
In this question, we will use the OpenWeather API to get the pollution data for different cities. Do the following:

Get a list of cities with their latitude and longitude information by doing the following:
(a) Download the list of cities from the table in https://en.wikipedia.org/wiki/List_of_cities_by_elevation using pd.read_html()
(b) Keep all the rows except those with Americas as Continental Region in a pd.DataFrame. Only keep columns City Name/s, Continental Region, Latitude and Longitude. How many cities do you have in the pd.DataFrame?
(c) Convert the Latitude and Longitude from the use of "N", "E", "S", "W" to float with signs +, +, -, -
At the end you should get a pd.DataFrame like the following:


Note only the first few rows are shown here.

Update the key.json file with your OpenWeather API key, read OpenWeather API price to find out how many API calls you can make per minute, per day and per month with your free account, and understand how to use the Air Pollution API by reading the documentation here

You do not need to provide an answer for this part, but above are preparation works that will be useful when you call the API later
Do the following:

(a) Make API calls using the Air Pollution API to collect the current air pollution data of the cities from (1) using the latitude and longitude information from (1)
(b) Combine the result from (1) and (3a) in a pd.DataFrame with the following 10 columns:
City name
Continental region
The concentration of 8 types of polluting gases and particulates (8 separate columns)
Carbon monoxide (CO), Nitrogen monoxide (NO), Nitrogen dioxide (NO2), Ozone (O3), Sulphur dioxide (SO2), Ammonia (NH3), and particulates (PM2.5 and PM10)
(c) Store the pd.DataFrame from (3b) into a csv file in the data folder, with the name of the file to be air_pollutant_2022mmdd.csv with mm the month and dd the day you have collected the data. This file will help us to verify your result
Use the pd.DataFrame from (3b) to investigate the relations between different variables by using some descriptive statistics like correlation and/or some aggregate functions:

If the concentration of one pollutant is high, is it more likely that the concentration of another pollutant is also high?
Do you find any relations between continental region and the pollution levels?
Please state the limitations of your answers.

Hints
For (1), you may find .apply() and/or .str.replace() useful
For (3), you may want to make use of .iterrows() to help you to iterate over each row
