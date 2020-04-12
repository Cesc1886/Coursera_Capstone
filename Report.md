# REPORT

## Compare the neighborhoods of New York and Toronto Based on k-means method

### Introduction
New York City and Toronto are very diverse and are the financial capitals of their respective countries.

My friend Mr. Wang works in Toronto and lives in a very good neighborhood. There are many popular venues around this neighborhood, but now he has a chance to work in New York, he hopes to find a neighborhood in New York that is very similar to the neighborhood in Toronto.

This Project uesd the data from internet to compare the neighborhoods of the two cities(New York City and Toronto) and determine how similar or dissimilar they are, meanwhile provide a solution for the users who are also interested in the features of neighborhoods in different cities. 

### Data Section
The dataset which has the main components Borough, Neighborhoods, Latitude and Longitude informations of the cities.
For the Toronto neighborhood data, a Wikipedia page exists that has all the information I need to explore and cluster the neighborhoods in Toronto. so I need to scrape the Wikipedia page and wrangle the data, clean it, and then read it into a pandas dataframe so that it is in a structured format.

For the New York neighborhood data, I found a geojson file from 'https://geo.nyu.edu/catalog/nyu_2451_34572' , so I got the New York City Neighborhood Names and also Borough, Latitude and Longitude informations.

For the venues around each neighborhood, I uesd Foursquare API to get the 100 nearest venues around each neighborhood for analysis.

The steps as below

1. obtain the data of Borough and Neighborhood in Toranto via 'https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M'
2. obtain the data of Latitude and Longitude in Toranto via geojson file.
3. obtain the data of Borough,Neighborhood Latitude and Longitude in New York via geojson file.
4. obtain the data of venues via Foursquare location data

### Methodology

The dataset which has the main components Borough, Neighborhoods, Latitude and Longitude informations of the cities.
at first, I need to make sure that I could get all informations that I need, so I scraped the Wikipedia page and wrangle the data, clean it, and then read it into a pandas dataframe so that it is in a structured format.

I also defined several functions to get the venues around each neighborhoods by using Foursquare API.
also, I used python folium library to visualize geographic details of the cities.
In the anlysis part, I used Cluster with K-Means Method

### Results
As we see, The neighborhoods in both of the cities are quite similar with the top 10 most commen venues. There 6 cluser of Neighborhoods in both of New York and Toronto.


### Discussion and Conclusion
In this Section I always have a question, How does K-means clustering algorithm deal with the problem of data noise and discrete feature processing? I do think the effect of outliers on unsupervised clustering is obvious, because it is necessary to learn the characteristics of the cluster while preventing the interference of outliers.
K-means and hierarchical clustering are very sensitive to outliers because they require each point to be divided into a cluster.
So, for the future work, I think there is a better way to slove this problem:
1. Density based clustering
2. Finite Mixture Models or Soft K-means
3. K-modes and K-prototypes, which have better performance for handling categorical variables.

