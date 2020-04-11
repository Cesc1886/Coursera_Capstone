# REPORT

## Based on k-means method to compare the neighborhoods of New York and Toranto

### Introduction
This Project compared the neighborhoods of the two cities(New York City and Toranto) and determine how similar or dissimilar they are. Both cities are very diverse and are the financial capitals of their respective countries.

Suppose you work in Toronto and you're happy with the neighborhood you live in, but you've got a job offer in New York, and you hope to find a neighborhood in New York with a high degree of similarity, and the results of this project will provide that possibility.

### Data Section
1. obtain the data of Borough and Neighborhood in Toranto via 'https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M'
2. obtain the data of Latitude and Longitude in Toranto via geojson file.
3. obtain the data of Borough,Neighborhood Latitude and Longitude in New York via geojson file.
4. obtain the data of venues via Foursquare location data

### Methodology
The dataset which has the main components Borough, Neighborhoods, Latitude and Longitude informations of the cities.
used Foursquare API to get the venues around each neighborhoods.
used python folium library to visualize geographic details of the cities.
Cluster with K-Means Method

### Results
The neighborhoods in both of the cities are similar with the top 10 most commen venues
