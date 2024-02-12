# 6_Python-APIs - WeatherPy and VacationPy

WeatherPy and VacationPy demonstrate the application of Python skills, APIs, and data visualization techniques to analyze and visualize weather data

WeatherPy:
- Visualize weather data for over 500 cities of varying distances from the equator
- Use citipy, OpenWeatherMap API, and codes to create a representative model of weather across cities

VacationPy:
- Use weather data to plan future vacations
- Employ Jupyter notebooks, GeoViews Python library, and Geoapify API to create map visualizations

###Note for Central Grader:
For WeatherPy Requirement 2: Compute Linear Regression for Each Relationship, I tried using both manual coding and plotting with the function. 
Therefore, you will see something like this on the codes. 
I am guessing the preferrable way is using the function, however, I won't be able to follow the psuedocodes line-by-line on the starter code file.
The manual coding also seem to be easier to adjust when it comes to the cosmetic look of it - for example: relocating the model's formula.

Method 1 - Manual Coding - the linear regression analysis is performed directly within the script without using the function
Linear regression on Northern Hemisphere
(slope, intercept, rvalue, pvalue, stderr) = linregress(northern_hemi_df["Lat"], northern_hemi_df["Max Temp"])
print(f"The r-value is: {rvalue}")
line_eq=f"y = {round(slope,2)}x + {round(intercept,2)}"

regress_values = northern_hemi_df["Lat"] * slope + intercept

plt.scatter(northern_hemi_df["Lat"], northern_hemi_df["Max Temp"])
plt.plot(northern_hemi_df["Lat"],regress_values,"r-")
plt.annotate(line_eq, ((5, -20)), fontsize=15, color="red") 

Incorporate the other graph properties
plt.xlabel("Latitude")
plt.ylabel("Temperature(C)")
plt.tight_layout()
plt.title("Northern Hemisphere: Temperature (C) vs. Latitude ")

Show plot
plt.show()

Method 2 - Linear regression on Northern Hemisphere using the function
linerWeather("Lat","Max Temp","north")

