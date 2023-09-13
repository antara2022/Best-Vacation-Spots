## Best-Vacation-Spots

![](Images/hotels_map_final_submission.png)

Map Visualization of Best Vacation Spots using APIs

During this project, I used concepts that I have learned about Python requests, APIs and JSON traversals to complete two challenges, WeatherPy and VacationPy to find out what the weather is like as we approach the equator. For WeatherPy, I created a Python script to visualize the weather of over 500 cities of varying distance from the equator. Using the Python library Citipy, the OpenWeatherMap API and problem-solving skills, I created a representative model of weather across cities. For VacationPy, I used my weather data skills to plan future vacations. I used Jupyter gmaps and the Google Places API to narrow down the cities found in part 1 based on ideal weather conditions for a vacation. I then created a heat map that also displays the hotel closest to these ideal vacation spots.

### Dataset:

 [Weather API](https://openweathermap.org/api),  [Google Maps API](https://mapsplatform.google.com/)

## Objective #1: Weather 

### Step 1 - Generate Cities List 

* Create list of cities from a random set of latitudes and longitudes using citipy

### Step 2 - Perform API Calls

* Perform weather check on each city using a series of successive API calls
    * Include print log of each city as it's being processed (with the city number and city name)

![](Images/city_list.png)

### Step 3 - Convert Raw Data to DataFrame

*  Export the city data into a .csv
*  Display the DataFrame 

![](Images/dataframe.png)

### Step 4 - Plot the Data 

* This scatterplot shows the relationship between the city's latitude and the maximum temperature

![](output_data/Fig1.png)

* This scatterplot shows the relationship between the city's latitude and the humidity

![](output_data/Fig2.png)

* This scatterplot shows the relationship between the city's latitude and the cloudiness

![](output_data/Fig3.png)

* This scatterplot shows the relationship between the city's latitude and the wind speed

![](output_data/Fig4.png)

### Step 5 - Linear Regressions 

![](output_data/linear-regression-northern-hem-temp-latitude.png)
    
![](output_data/linear-regression-southern-hem-temp-latitude.png)

* After viewing these two plots, the linear regression is modeling that there is a strong negative correlation between max temp and latitude in the Northern Hemisphere, while there is a strong positive correlation between max temp and latitude in the Southern Hemisphere.
    
![](output_data/linear-regression-northern-hem-humidity-latitude.png)
    
![](output_data/linear-regression-southern-hem-humidity-latitude.png)

* After viewing these two plots, the linear regression is modeling that there is no correlation between humidity and latitude in the Northern and Southern Hemispheres.
    
![](output_data/linear-regression-northern-hem-cloudiness-latitude.png)
    
![](output_data/linear-regression-southern-hem-cloudiness-latitude.png)

* After viewing these two plots, the linear regression is modeling that there is a weakly positive correlation between cloudiness and latitude in the Northern Hemisphere, while there is no correlation between cloudiness and latitude in the Southern Hemisphere.
    
![](output_data/linear-regression-northern-hem-wind-speed-latitude.png)
    
![](output_data/linear-regression-southern-hem-wind-speed-latitude.png)

* After viewing these two plots, the linear regression is modeling that there is a weakly positive correlation between wind speed and latitude in the Northern Hemisphere, while there is no correlation between wind speed and latitude in the Southern Hemisphere.

---------------------------------------------------

## Objective #2: Vacation

### Step 1 - Store Part I results into DataFrame

* Load the csv exported in Part I:Weather into a DataFrame

![](Images/vacation-dataframe.png)

### Step 2 - Humidity Heatmap

* Configure gmaps
* Use the Lat and Lng as locations and Humidity as the weight
* Add Heatmap layer to map

![](Images/heatmap_screenshot_final_submission.png)

### Step 3 - Create New DataFrame Fitting Weather Criteria

*  Narrow down the cities to fit weather conditions
    * A max temperature lower than 80 degrees but higher than 70
    * Wind speed less than 10 mph
    * Zero cloudiness
*  Drop any rows will null values

![](Images/vacation-dataframe2.png)

### Step 4 - Create Hotel Map

* Add a "Hotel Name" column to the DataFrame
* Set parameters to search for hotels with 5000 meters
* Hit the Google Places API for each city's coordinates
* Store the first Hotel result into the DataFrame
* Plot markers on top of the heatmap

![](Images/hotels_map_final_submission.png)

---------------------------------------------------

<b>Contact:</b> antara.choudhury3000@gmail.com
