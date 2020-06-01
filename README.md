# Weather dashboard
## Homework assignment no. 6 | U of T Full-Stack Coding

### 1. Summary
This application is a weather dashboard that allows the user to look up a city and view current weather conditions as well as a forecast for the next five days. The overview of the current condition also includes a color-coded UV index to show the potential risk of UV radiation on that day. Cities that have been searched for are being stored in the search history, which is accessible in a side navigation. The cities are also being stored in local storage, so they persist reloading the page. Upon reload, the most recently queried city will show.
![Screenshot of the application](https://github.com/cestmarcel/uoft-weather/blob/master/assets/screenshots/application.png)

### 2. Page components
#### 2.1 City search
The city search takes in the name of the city and converts it into longitude and latitude using the OpenCage Geocoder API (see below). Cities that have been searched for will be added to the search history, which is also visualized on the page. When the user later clicks on one of the cities, the weather info for that city will be loaded.
![Screenshot of the application](https://github.com/cestmarcel/uoft-weather/blob/master/assets/screenshots/cities.png)

#### 2.2 Error message
If the user enters an invalid city name, they will be notified by a Bootstrap alert (more on Bootstrap below).
![Screenshot of the error alert](https://github.com/cestmarcel/uoft-weather/blob/master/assets/screenshots/error.png)

#### 2.3 UV warnings
In the overview of the current weather conditions, the user will find a color coded UV index, which indicates the intensity of UV radiation on that given day. The color coding has been implemented according to Sun Safety US (https://www.epa.gov/sunsafety/uv-index-scale-0).
![Screenshot of the uv index visualization](https://github.com/cestmarcel/uoft-weather/blob/master/assets/screenshots/uv-examples.png)

#### 2.4 5 day forecast
For each queried city, the user will also find a 5 day forecast on the bottom of the page. It shows an icon representing the weather conditions on that day as well as the projected temperature and humidity.
![Screenshot of the forecast section](https://github.com/cestmarcel/uoft-weather/blob/master/assets/screenshots/forecast.png)

#### 2.5 Clearing search history
The user can clear the search history by clicking the respective button underneath the search history buttons. They will have to confirm their choice through a Bootstrap modal. The latter has been implemented to prevent accidental clearing of the search history.
![Screenshot of the clearing modal](https://github.com/cestmarcel/uoft-weather/blob/master/assets/screenshots/modal.png)

### 3. External APIs, Framworks, and Libraries
- This application uses Bootstrap, utilizing responsive Styles and components. More information about Bootstrap is available under https://getbootstrap.com with documentation under https://getbootstrap.com/docs/4.5/getting-started/introduction/
- The weather dashboard uses weather data from Open Weather Map (https://openweathermap.org/), specifically the "One Call API" with documentation under: https://openweathermap.org/api/one-call-api 
- Geocoding is provided by OpenCage Data (https://opencagedata.com/). Documentation is available under: https://opencagedata.com/api
- This application also uses moment.js https://momentjs.com/ to access and format the current date and to display the dates for the 5 day forecast. Documentation for moment.js is available under: https://momentjs.com/docs/