<a id="anchor"></a>
# FLUTTER
## Weather App
![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)
---
## Description
It shows basic weather information, including the current status icon, temperature, weather description, sunrise and sunset times, and maximum and minimum temperatures.
***

## Main functions:

A Flutter application for displaying current weather functions as follows:

1. **Main file (main.dart)**:
 - The application is initialized using `runApp(const MyApp())`.
 - The `MyApp` class creates a `MaterialApp` that uses `FutureBuilder` to get the device's current geolocation.
 - If geolocation is available, a `BlocProvider` is initialized for `WeatherBlocBloc`, which requests weather data based on the device's current position.
 - If geolocation is not available, a loading indicator is displayed.

2. **Definition of position**:
 - The `_determinePosition` function uses the `geolocator` library to obtain the current position of the device.
 - If location services are disabled or you don't have the required permissions, an error is returned.

3. **Bloc and states (weather_bloc_bloc.dart)**:
 - `WeatherBlocBloc` manages the state of the application, responsible for requesting and retrieving weather data.
 - The `WeatherBlocSuccess` state contains information about the current weather, which is used to update the user interface.

4. **Home page (home_page.dart)**:
 - The `HomePage` class displays the current weather, including weather icon, temperature, description, sunrise and sunset times, maximum and minimum temperature.
 - Depending on the time of day, the background color changes.
 - The `getWeatherIcon` method selects an appropriate icon to display based on the weather condition code.
 - BlocBuilder monitors WeatherBlocBloc states and updates the interface based on the current state.

5. **Change the background depending on the time of day**:
 - Inside the `HomePage`, the background color defined in the `Align` containers changes depending on the current time of day. This allows you to visually distinguish the time of day and night.

<!-- 6. **Using the Intl library**:
 - The `intl` library is used to format date and time. For example, sunrise and sunset times are displayed in a user-friendly format. -->

Thus, the application provides an intuitive interface to display the current weather based on the user's geolocation, adapting the background depending on the time of day for a more natural experience.

## Elements
  
* AppBar + Text Widget
* Row
* Align
* BlocBuilder
* WeatherBlocBloc
* WeatherBlocEvent
* WeatherBlocState
* Text 

## Video

[![Example](<img width="327" alt="WA" src="https://github.com/RushMarina/FLUTTER-Weather/assets/150655218/b40b7b4a-204c-4ce4-917e-dfe9aa5bbfba">)]

___
[Up](#anchor)
