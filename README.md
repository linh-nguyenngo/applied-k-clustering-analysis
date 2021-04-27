# An data analysis project to discover potential locations for new restaurant in Torontto
## Introduction
Toronto is one of the greatest cities in the world to do business, consistently ranked at the top when it comes to global competitiveness, innovation and quality of life. A foreign restaurant chain wants to open new locations in Toronto but they do not have any experience with the city. Thus, they want to explore the neighborhoods of this city so that they can make an informed decision for the business. The deciding factor for most would be on the liveliness of each of the neighborhood and the differences between them. The company seeks for data-driven solution as a major part in their decision-making process. 

## Data description
Data Link: https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M
For our study we need data about neighborhoods in the city. The neighborhood data of the city of Toronto is not readily available on the internet. But, a Wikipedia page exists that has all the information we need, to explore and cluster the neighborhoods. so we have to scrape the Wikipedia page and wrangle the data, clean it, to be converted into a structured format so that it can be read into a pandas dataframe. We can then use the geopy library or a readily available csv file which contains the coordinates of the postal codes to get the latitude and longitude values of boroughs of Toronto. We can then create a map of Toronto with neighborhoods superimposed on top by using the Visualization library Folium. Now we can finally focus our attention to the borough Downtown Toronto and can explore further the neighborhood that the city has to offer. We can use Foursquare API's by using our credentials to get the categories or venues of each neighborhood within a particular radius of say 5oomts and can find the top 10 most common venues from these neighborhoods which will help us to know the most common venues from these neighborhoods.
Now after finding the most common venue from Downtown Toronto, Toronto we can compare the neighborhoods. 

## Methodology
Clustering Approach:
To compare the neighborhoods, we decided to explore them, segment them, and group them into clusters. To be able to do that, we need to cluster data which is a form of unsupervised machine learning: k-means clustering algorithm.
Using K-Means Clustering Approach : We using K-means clustering to cluster the unlabel dataset neighborhood from several category in Foursquare API.

## Result
Map clustering result of Downtown area

By spotting the clusters of items we can see which neighborhood has density of restaurant business. THen, we explore closer into smaller neighborhoods of Downtown and list top 10 most common venues of each labelled area. 

For Downtown Toronto Clusters:
Label 0: Very few neighborhoods fall to this cluster. The neighborhoods belonging to this cluster are popular for having coffee shops, restaurants, Cafes, park and pub.
Label 1: Very few neighborhoods fall to this cluster. The neighborhoods belonging to this cluster are popular for having park, playground, yoga studio, dance studio etc.
Label 2: There are many neighborhoods which fall to this cluster. The neighborhoods belonging to this cluster are popular for having coffee shops, cafe's, Different cuisine restaurants(American, Italian, Japanese etc), Bar, pub etc
Label 3: Very few neighborhoods fall to this cluster. The neighborhoods belonging to this cluster are popular for having Airport Lounge, Airport Service, Airport Terminal, Boat Ferry, Rental car location etc.
Label 4: Very few neighborhoods fall to this cluster. The neighborhoods belonging to this cluster are popular for having Grocery store, candy store, baby store, park, restaurant, Athletic&Sports, cafe.

## Recommendation 
We see that neighborhoods of Label2 has a lot of foreign cuisine restaurants. So opening a restaurant here will face high competition.
Also, neighborhoods of Label1 Downtown toronto provides for some recreational places such as Gyms, Parks, yoga studio, dance studio etc , so there is opportunity for the restaurant to attract customers.
Also by looking at the venues of Label3 of Downtown Toronto it seems like it is nearby airport, so opening a restaurant here is ok but not the best option. 
