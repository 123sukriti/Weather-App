# Weather-App

## Introduction
Hello there! 👋 I'm **Sukriti Das**, the developer behind this Weather App. I'm passionate about creating user-friendly applications and making technology accessible to everyone.

## About Me
I am  **2nd year Btech CSE student**, and I enjoy combining my technical skills with creativity to build innovative solutions. This project is a result of that passion, and I hope it serves as a useful tool for checking real-time weather conditions effortlessly.

## Project Overview
This Weather App is a simple and intuitive tool that allows users to check the current weather conditions based on their location or by searching for a specific city. The application is built using HTML, CSS, and JavaScript, making use of the DOM manipulation concept to create a dynamic user interface. It also leverages the OpenWeatherMap API to fetch real-time weather data.

## Description
This project is a simple weather application that allows users to check the current weather conditions based on their location or by searching for a specific city. The application is built using HTML, CSS, and JavaScript, leveraging the DOM manipulation concept to create a dynamic user interface. It also makes use of the OpenWeatherMap API to fetch real-time weather data.

## Features
- **User Location:** The app uses the Geolocation API to get the user's coordinates and fetches weather information based on their location.
- **Search Functionality:** Users can also search for weather information in a specific city by entering the city name.
- **Dynamic UI:** The user interface dynamically updates to display weather details, including temperature, description, wind speed, humidity, and cloudiness.

## Technologies Used
- **HTML:** Structuring the webpage.
- **CSS:** Styling the user interface for an enhanced user experience.
- **JavaScript:** Implementing the functionality and manipulating the DOM.
- **OpenWeatherMap API:** Fetching real-time weather data.

## Project Setup
1. Clone the repository: `git clone https://github.com/yourusername/weather-app.git`
2. Open the `index.html` file in a web browser.

## Usage
1. **Grant Location Access:** Click on the "Grant Access" button to allow the app to access your current location.
2. **Search for a City:** Enter the name of the city in the search bar and press Enter to get weather information for that city.

## How to Contribute
If you want to contribute to this project, follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Make your changes and commit them: `git commit -m 'Add a new feature'`.
4. Push to the branch: `git push origin feature/new-feature`.
5. Submit a pull request.

### Code Snippets
Here are some key code snippets from the project:

#### JavaScript for Getting User's Location:
```javascript
function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition);
    } else {
        alert("Geolocation is not supported by your browser");
    }
}

function showPosition(position) {
    const userCoordinates = {
        lat: position.coords.latitude,
        lon: position.coords.longitude,
    }

    sessionStorage.setItem("user-coordinates", JSON.stringify(userCoordinates));
    fetchUserWeatherInfo(userCoordinates);
}

const grantAccessButton = document.querySelector("[data-grantAccess]");
grantAccessButton.addEventListener("click", getLocation);


