# Weather App

This is a simple web application that fetches and displays weather information based on the user's input or their current location.

## Features

* **Search by City:** Users can enter a city name to retrieve the current weather conditions for that city.
* **Use Current Location:** Users can allow the app to access their device's location to get weather information for their immediate area.
* **Displays Weather Details:** The app shows the following weather information:
    * City Name and Country
    * Weather Description (e.g., "clear sky", "rain")
    * Temperature (in Celsius)
    * Humidity
    * Wind Speed

## Technologies Used

* HTML: For structuring the web page.
* CSS: For styling the web page and providing a user-friendly interface.
* JavaScript: For handling user interactions, fetching data from the OpenWeatherMap API, and dynamically updating the page content.
* OpenWeatherMap API:  To retrieve weather data.

## Setup

To run this application:

1.  Save the provided HTML code as `weather.html`.
2.  Open the `weather.html` file in a web browser.

## API Key

* The application uses the OpenWeatherMap API to fetch weather data.  
* **Important:** You will need to replace `"55a373c572d6fae5301da64e178cd525"` with your own API key from OpenWeatherMap for the application to function correctly.  You can obtain a free API key by signing up at [https://openweathermap.org/api](https://openweathermap.org/api).

## How it Works

1.  **User Interaction:**
    * The user enters a city name in the input field and clicks the "Search" button.
    * OR
    * The user clicks the "Use My Location" button to use their device's geolocation.

2.  **Fetching Weather Data:**
    * If the user searches by city, the `fetchWeather` function is called with the city name.  This function constructs an API request to OpenWeatherMap using the city name and the API key.
    * If the user uses their location, the browser's `navigator.geolocation` API is used to get the user's latitude and longitude.  Then, an API request is made to OpenWeatherMap using the coordinates and the API key.

3.  **Displaying Weather Data:**
    * The API response is parsed as JSON.
    * The `showWeather` function updates the HTML content of the `result` div with the relevant weather information (city, country, description, temperature, humidity, wind speed).
    * If there's an error fetching the weather data (e.g., invalid city name), an error message is displayed in the `result` div.

## Styling

* The application uses inline CSS styles within the `<head>` section of the HTML file.
* The styles provide a centered layout, a gradient background, a styled "weather card" to display information, and basic styling for form elements and the result display.

## Notes

* Error handling is included to manage cases where the API request fails or the user enters an invalid city name.
* The temperature is displayed in Celsius, and the wind speed is in meters per second.
* The design is responsive to some extent, but further improvements could be made for better cross-device compatibility.
