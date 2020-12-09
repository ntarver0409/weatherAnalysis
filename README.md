# weatherAnalysis and vacationAnalysis
weatherAnalysis.ipynb: This code is designed to scrape the information of 600+ cities from a random list of coordinates from open weather API, export that information to a dataframe/csv, and the plot and analyze the data. In this I analyzed the relationship between latitude and max temperature, latitude and humidity, latitude and cloudiness, and latitude and wind speed. I then plotted and ran a regression for the same plots in the northern and southern hemipshere.

A couple of things I noticed when analyzing this data:

1. There is a strong coorelation between latitude and temperature in the northen hempisphere (r-squared = 0.75) but strangely as much in the southern hemisphere (r-squared = 0.40). Based on pre-existing knowledge and looking at the overall data and what we see in the northern hemisphere you would expect a stonger coorelation. I think this may just be a random sampling quirk skewing the data but more tests should be ran to make sure.

2. I was surprised to see that the coorelation between latitude and correlation was so weak. In the northern hemisphere there was only a r-squared value of 0.12 and it was even weaker in the southern hemisphere with a regression value of 0.10. I had assumed that with the temps rising the humidity would also rise, but now Id think that proximity to water and other factors would influence it more.

3. The is pretty much no relation between latitude and cloudiness of wind speed. It would seem that the rise or fall in themperature related to latitude simply has no effect on these variables.


vacationAnalysis.ipynb: In this code I took the ouputted csv and made a google maps heat map charting the humidity of all those locations. Then it whittles down the csv to to find cities with my ideal conditions and pulled the google places API to find the closest hotel to that city to put that into a dataframe. Then it make a new layer for my google maps figure with markers on each city that contain the hotel name, city, and country name.
