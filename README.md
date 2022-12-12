# Seattle Neighborhoods: An Interactive Guide

## Project description

- This web map application, built using Mapbox GLJS, allows users to easily find and visualize important information about a specific location. With the ability to enter an address, the map will quickly geocode the location and display it on the interactive map. 
- The map contains four layers of information: education, flood, housing prices, and crime. This allows users to see the education options in the area, whether it is at risk for flooding, the housing prices in the area, and the crime rates. Each layer can be turned on or off depending on the user's needs.
- With the combination of geocoding and multiple layers of information, this map provides a comprehensive view of a specific location and is a valuable tool for anyone looking to learn more about an area.

## Project goal

- The targeted audience for our project can be people looking at the housing market for Seattle, possibly aiming to buy a house. Another target audience would be government policy makers deciding how to allocate funding for social/educational programs in Seattle. So policy makers could view the relationship between certain neighborhoods and crime rates or academic success to determine the amount and type of funding for that neighborhood. The goals of this webmap application are to provide those target audiences with a comprehensive view of a specific location, by allowing them to easily find and visualize important information about an address. In conclusion, by combining geocoding with multiple layers of information, such as education, flood risk, housing prices, and crime rates, the map helps users make informed decisions about an area.

- Additionally, the ability to turn each layer on or off allows users to customize the map to their specific needs, making it a valuable tool for anyone looking to learn more about a location. Whether you are a potential homeowner, a business owner, or simply curious about a specific area, this webmap has the information you need.

## The application URL

**[Seattle Neighborhoods: An Interactive Guide](https://leofanguw.github.io/Seattle_Housing_BA2/)**

## Screenshots

## Main functions
- The main functions of this webmap application are to provide users with a comprehensive view of a specific location and to allow them to easily find and visualize important information about an address. Since the target audiences include people looking at the housing market, we assume our audiences want to view multiple addresses at the same time. For example, our audiences may want to compare the housing conditions between two different places, so the functionality of adding multiple pins at the same time is necessary. We’ve changed the default geocoder in Mapbox, now every address our audiences searched for will be saved, and they can use the clean button to clean their search history.
- In addition to this core function, the map also includes an interactive feature where users can click on individual map elements to view more detailed information about them. For example, if a user clicks on an item in the school layer, they can see the school's name, what type of school it is, and whether the school is public or private.
- The map also includes a side menu that allows users to easily enable or disable different layers, allowing users to customize the map to their specific needs and preferences. Multiple layers can be turned on at the same time, allowing users to compare and contrast various features between the layers.

## Data sources

- The Flood Zone layer comes from the Flood Zones ECA dataset. This source guarantees those flood zones have a one percent or greater chance of being covered with or of carrying water in any given year based on current circumstances. It will help our target audience define the potential housing risk caused by the natural environment, and our audience can compare this flood layer with other layers to visualize the whole situation.
- The Education layer of our map contains data from two datasets that were merged together. This file contains data from the Seattle Open Data Portal Public Schools and Private Schools datasets. This data comes from the Seattle Open Data Portal and was used to create the education layer in the webmap. To merge these files, several columns of data were removed in order to ensure that the resulting geojson file contains data present in both data sources. The Name column shows the name of the schools. The Status column provides information on whether the school is public or private, and additional details on the type of school it is. The PublicPrivate column specifies whether the school is from the Private School dataset or the Public School dataset. This information will be displayed when the education layer is active and the user clicks on a school.
- The Crime layer of our map contains data from SPD Crime Data: 2008-Present. Due to the original dataset being very large, it was reduced down to just the most recent year of 2021 and limiting to more violent crimes (assault offenses, arson, robbery, larceny). One point of data displays the type of crime it is and where in Seattle it happened. This layer is intended to inform users where in Seattle may be more violent than other areas or if a type of violent crime occurs more often in certain locations.
- The Housing Cost layer of our map contains data from the House Sales in King County, USA dataset. The original dataset was trimmed down to house sales from the year 2015 as it was the latest year in the dataset. Additionally, unnecessary columns were removed from the original dataset and only relevant columns that help depict the housing costs of the house sale were kept such as the price, living square footage, and the cost per square foot. When the user clicks on the house sale circle and the housing cost layer is active these columns of information from the dataset will be shown. Access to this information will allow the user to determine the general trend of housing costs in an area when compared to other nearby points or nearby neighborhoods.

## Applied libraries

- [mapbox gl js](https://api.tiles.mapbox.com/mapbox-gl-js/v2.5.1/mapbox-gl.js)
- [mapbox gl css](https://api.tiles.mapbox.com/mapbox-gl-js/v2.5.1/mapbox-gl.css)
- [mapbox gl js-geocoder](https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-geocoder/v4.7.0/mapbox-gl-geocoder.min.js)
- [mapbox gl css-geocoder](https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-geocoder/v4.7.0/mapbox-gl-geocoder.css)
- [hamburger button](https://github.com/jonsuh/hamburgers)


## Acknowledgment

- We really appreciate the help from [Mapbox](https://www.mapbox.com/) for providing APIs.
- We really appreciate the help from [Hamburgers](https://github.com/jonsuh/hamburgers) for style fixing.
- We really appreciate the dataset from [Flood Zones ECA](https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::flood-zones-eca/explore?location=47.584721%2C-122.255554%2C11.08), [Public Schools](https://data.seattle.gov/dataset/Seattle-Public-Schools-Sites-2022-2023/bd7c-x34g) & [Private Schools](https://data.seattle.gov/dataset/Private-Schools/ftp7-mj2b), [SPD Crime Data: 2008-Present](https://data.seattle.gov/Public-Safety/SPD-Crime-Data-2008-Present/tazs-3rd5) and [House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction?resource=download)

## Other things that are necessary to inform the audience

> One important thing to mention here is we don’t include a time frame in this final project, because for our target audiences, we want to provide the most recent and relevant information. For example, instead of making a time slider from 2000 to 2015, we only include the house sales in 2015 as a layer. Because for users or policy makers looking at the housing market, it’s less meaningful to reference the data years ago. Or we will just include datasets that are highly-recapitulative, such as the flood zones. Those flood zones have a one percent or greater chance of carrying water in any given year.