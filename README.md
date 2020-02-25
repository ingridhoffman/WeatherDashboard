# Homework6

Server-Side APIs: Weather Dashboard

## Assignment

Developers are often tasked with retrieving data from another application's API and using it in the context of their own. Third-party APIs allow developers to access their data and functionality by making requests with specific parameters to a URL. Your challenge is to build a weather dashboard that will run in the browser and feature dynamically updated HTML and CSS.

Use the [OpenWeather API](https://openweathermap.org/api) to retrieve weather data for cities. The documentation includes a section called "How to start" that will provide basic setup and usage instructions. Use `localStorage` to store any persistent data.

### User Story

```
AS A traveler
I WANT to see the weather outlook for multiple cities
SO THAT I can plan a trip accordingly
```

### Acceptance Criteria

```
GIVEN a weather dashboard with form inputs
WHEN I search for a city
THEN I am presented with current and future conditions for that city and that city is added to the search history
WHEN I view current weather conditions for that city
THEN I am presented with the city name, the date, an icon representation of weather conditions, the temperature, the humidity, the wind speed, and the UV index
WHEN I view the UV index
THEN I am presented with a color that indicates whether the conditions are favorable, moderate, or severe
WHEN I view future weather conditions for that city
THEN I am presented with a 5-day forecast that displays the date, an icon representation of weather conditions, the temperature, and the humidity
WHEN I click on a city in the search history
THEN I am again presented with current and future conditions for that city
```

The following image demonstrates the application functionality:

![weather dashboard demo](./Assets/06-server-side-apis-homework-demo.png)

## Developer Notes

Added functionality to open page with weather at current user location (if geolocation is available)

### HTML

- Header with Page Title
- Sidebar with City Search and list of search history
- Primary content with name of City, date, icon for current condition, temperature, humidity, wind speed and color coded UV index
- Secondary content with five-day forecast grid - individual boxes for each day that include date, icon of conditions, temperature, and humidity

### CSS

- Bootstrap responsive styling

### Script Logic

```
Globals
- Variable for Current City
- Array for search history
- API Key

Set Current City
- Get user entry from search box
- Get user entry from history list

Make API Call
- Custom query URL with variables for City and API Key

Get Data
-


Local Storage
- Get search history when page is opened or refreshed
- Update history array when user does a search - verify search is for City not already on list

```

### Known Issues

- can't use Return button to search - it refreshes page instead
- text doesn't clear from text entry box when search button is clicked
- new city should be added to search history at top insetad of bottom
- city should not be added to search history if already present
- history should be limited?

### Acknowledgements

### Application URL
