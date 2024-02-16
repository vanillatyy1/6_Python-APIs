# 6_Python-APIs - WeatherPy and VacationPy

WeatherPy and VacationPy demonstrate the application of Python skills, APIs, and data visualization techniques to analyze and visualize weather data

WeatherPy:
- Visualize weather data for over 500 cities of varying distances from the equator
- Use citipy, OpenWeatherMap API, and codes to create a representative model of weather across cities

VacationPy:
- Use weather data to plan future vacations
- Employ Jupyter notebooks, GeoViews Python library, and Geoapify API to create map visualizations

## Note for Central Grader:
### 1) RE: Feedback Feb 14 at 10:43pm

The "Generate the Cities List by Using the `citipy` Library" part of the code is given by the starter file, but you mentioned that the the expected output for cities is 611 as per Feb 14 at 10:43pm feedback.
However the list is based on random, and Part 1 WeatherPy's instruction only say "over 500 cities". 
I tried re-generating for a few times, and the closest I could get is 610.
Would that be sufficient?

### 2) WeatherPy Requirement 2
For WeatherPy Requirement 2: Compute Linear Regression for Each Relationship, I tried using both manual coding and plotting with the function. 
I am guessing the preferrable way is using the function, however, I won't be able to follow the psuedocodes line-by-line on the starter code file.
The manual coding also seem to be easier to adjust when it comes to the cosmetic look of it - for example: relocating the model's formula.

Therefore, I have decided to display the input and output of both methods.

![Image Description](https://github.com/vanillatyy1/6_Python-APIs/blob/918ed520c15fbb2878768c25b63326a3a868b82c/Screenshot_for_readme/example1.png)

![Example Image](https://github.com/vanillatyy1/6_Python-APIs/blob/main/Screenshot_for_readme/example.png)

Plot with Method 1:

![Northern Hemisphere Temperature vs Latitude - Method 1](https://github.com/vanillatyy1/6_Python-APIs/blob/main/Screenshot_for_readme/Northern%20HemisphereTempC%20vs%20Latitude_method1.png)

Plot with Method 2:

![Northern Hemisphere Temperature vs Latitude - Method 2](https://github.com/vanillatyy1/6_Python-APIs/blob/main/Screenshot_for_readme/Northern%20HemisphereTempC%20vs%20Latitude_method2.png)

## CityPy:
'see VacationPy.ipynb'

### City Data Retrieval:
- Generated random geographic coordinates
- Utilized citipy to find the nearest city to each coordinate
    'Current output: 610
- Retrieved weather data for each city using the OpenWeatherMap API
- Created a DataFrame to store city weather data
  
| Column      | Count |
|-------------|-------|
| City        | 582   |
| Lat         | 582   |
| Lng         | 582   |
| Max Temp    | 582   |
| Humidity    | 582   |
| Cloudiness  | 582   |
| Wind Speed  | 582   |
| Country     | 582   |
| Date        | 582   |

### Weather Visualization:
- Created scatter plots to showcase the relationship between latitude and various weather variables (Temperature, Humidity, Cloudiness, Wind Speed)

### Linear Regression Analysis:
- Computed linear regression for each weather variable
- Separated plots into Northern and Southern Hemispheres
- Created scatter plots with linear regression lines, equations, and r-values

### Discussion on Linear Relationships:
- Analyzed the relationship between latitude and weather variables in both hemispheres
- Interpreted the linear regression results to understand how temperature, humidity, cloudiness, and wind speed change with distance from the equator

## VacationPy:
### City Map Visualization:

- Created a map displaying points for every city in the DataFrame
- Adjusted the size of the points based on humidity levels

![City Map](https://github.com/vanillatyy1/6_Python-APIs/blob/fd70e8d47c83003a5eeb05c3c15b96f2b67e49d1/Screenshot_for_readme/city_map.png)

### Ideal Weather Condition Selection:

- Narrowed down cities based on preferred weather conditions (sunny, moderate temperature)
- Created a DataFrame with selected cities

| City_ID | City           | Lat      | Lng      | Max Temp | Humidity | Cloudiness | Wind Speed | Country | Date       |
| ------- | -------------- | -------- | -------- | -------- | -------- | ---------- | ---------- | ------- | ---------- |
| 26      | dolores        | -36.3132 | -57.6792 | 25.72    | 53       | 0          | 5.09       | AR      | 1708097680 |
| 64      | howrah         | 22.5892  | 88.3103  | 24.00    | 73       | 0          | 2.06       | IN      | 1708097684 |
| 99      | east london    | -33.0153 | 27.9116  | 24.52    | 46       | 0          | 4.12       | ZA      | 1708097693 |
| 191     | pucon          | -39.2822 | -71.9543 | 24.27    | 48       | 1          | 1.71       | CL      | 1708097707 |
| 217     | kone           | -21.0595 | 164.8658 | 24.33    | 86       | 4          | 2.55       | NC      | 1708097711 |
| 248     | dakhla         | 23.6848  | -15.9580 | 23.01    | 60       | 0          | 11.83      | EH      | 1708097716 |
| 255     | port elizabeth | -33.9180 | 25.5701  | 23.16    | 53       | 0          | 12.35      | ZA      | 1708097717 |
| 258     | sur            | 22.5667  | 59.5289  | 23.75    | 50       | 3          | 3.36       | OM      | 1708097718 |
| 263     | queenstown     | -31.8976 | 26.8753  | 23.17    | 12       | 3          | 8.52       | ZA      | 1708097718 |
| 279     | khasab         | 26.1799  | 56.2477  | 24.55    | 69       | 6          | 1.49       | OM      | 1708097720 |
| 362     | tadine         | -21.5500 | 167.8833 | 25.50    | 79       | 7          | 8.58       | NC      | 1708097731 |
| 366     | moog           | 8.6011   | 124.4658 | 24.89    | 86       | 8          | 3.09       | PH      | 1708097732 |
| 379     | mandideep      | 23.0817  | 77.5333  | 23.49    | 31       | 10         | 2.19       | IN      | 1708097733 |
| 525     | necochea       | -38.5473 | -58.7368 | 25.85    | 50       | 0          | 4.38       | AR      | 1708097750 |
| 527     | malvan         | 16.0667  | 73.4667  | 25.44    | 75       | 4          | 3.99       | IN      | 1708097751 |
| 566     | sultanah       | 24.4926  | 39.5857  | 23.25    | 15       | 0          | 7.72       | SA      | 1708097755 |

### Hotel Search and Mapping:

- Utilized the Geoapify API to find hotels within a specified radius of each city
- Created a DataFrame to store city, country, coordinates, humidity, and hotel name
- Plotted hotels on the map with hover messages displaying city, country, humidity, and hotel name

![Hotel Map](https://github.com/vanillatyy1/6_Python-APIs/blob/fd70e8d47c83003a5eeb05c3c15b96f2b67e49d1/Screenshot_for_readme/hotel_map.png)

