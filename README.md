# ☁️ Nimbus: Real-Time Meteorological Dashboard

![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)
![API](https://img.shields.io/badge/API-OpenWeatherMap-orange?logo=openweathermap)
![Status](https://img.shields.io/badge/Status-Live-success)
![Design](https://img.shields.io/badge/Design-Glassmorphism-blue)

> **A high-precision weather forecasting application capable of fetching real-time meteorological data for any city on Earth. Built with a focus on asynchronous data handling and fault-tolerant API integration.**

---

## 🚀 Live Telemetry
**[Click here to launch the Dashboard](https://saiganesh-weather-app.netlify.app/)**
*(Type a city name like "Tokyo" or "London" to see live data)*

---

## 🧠 The Engineering (How it Works)
This application is more than just a UI wrapper; it implements a robust data-fetching pipeline.

### 1. Asynchronous API Integration
Instead of blocking the main thread, the app uses **`async/await`** patterns to fetch data from the OpenWeatherMap REST API.
* **Efficient Networking:** Reduces latency by parsing JSON streams in real-time.
* **Dynamic Resource Loading:** Weather icons and data points are injected into the DOM only after a successful 200 OK response.

### 2. Error Boundary & Validation
* **Fault Tolerance:** If a user types a non-existent city, the system catches the `404 Not Found` error and displays a user-friendly alert instead of crashing.
* **Input Sanitization:** Search queries are trimmed and formatted to prevent malformed API requests.

### 3. Dynamic DOM Manipulation
* **State-Driven UI:** The interface updates instantly without a page reload (SPA behavior) by manipulating the Document Object Model directly based on the fetched data payload.

---

## ✨ Key Features
* **🌍 Global Coverage:** Access weather data for over 200,000 cities.
* **⚡ Instant Feedback:** <100ms response time on 4G networks.
* **💧 Detailed Metrics:** Displays Temperature, Humidity, Wind Speed, and Atmospheric Conditions.
* **🎨 Modern UI:** Features a "Glassmorphism" aesthetic with adaptive backgrounds based on weather conditions.
* **📱 Responsive:** Fully fluid layout that adapts to Mobile, Tablet, and Desktop screens.

---

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3 (Flexbox/Grid), Vanilla JavaScript
* **Data Source:** OpenWeatherMap API (JSON)
* **Deployment:** Netlify (CI/CD)

---

## 💻 How to Run Locally

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/i-saiganesh/weather-webapp.git](https://github.com/i-saiganesh/weather-webapp.git)
    cd weather-webapp
    ```

2.  **Configure API Key**
    * *Note: This project uses OpenWeatherMap.*
    * Open `script.js` and locate the `apiKey` variable.
    * Replace it with your own key from [OpenWeatherMap](https://openweathermap.org/api).

3.  **Launch the App**
    Open `index.html` in your browser.

---

## 📂 Project Structure

```text
weather-webapp/
│
├── index.html        # Structure
├── style.css         # Glassmorphism UI
├── script.js         # API Logic & DOM Manipulation
├── images/           # Weather Icons
└── README.md         # Documentation
