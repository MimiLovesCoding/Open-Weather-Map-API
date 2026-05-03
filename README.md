# ⛅🌈 AccuWeather API—Comprehensive API Test Suite☀️☔

<hr>

A full-cycle API validation project using Postman and the AccuWeather API, covering functional testing, negative/edge case testing, response validation, and structured test case documentation.

🔐 API keys, request headers, and body parameters have been omitted from all documentation for security purposes.

<hr>

##  📋 Project Overview <br>
This project validates the reliability, accuracy, and robustness of the AccuWeather API endpoints through a structured test suite. Testing included both positive scenarios (verifying expected behavior) and negative/stress scenarios (intentionally attempting to break the API to identify vulnerabilities and failure handling).
The API was confirmed to be robust, well-designed, and compliant with expected standards across all tested scenarios.<br>
<hr>

## 🛠 Tools & Technologies <br>
| Tools | Purpose |
| :--- | :--- |
| [ Postman](https://postman.com) | API client for building, executing, and documenting test calls |
|[Accuweather API](https://developer.accuweather.com/core-weather/location-key-currentconditions) | Third-party REST API providing real-time global weather data |
| Microsoft Excel |Structured test case management and results tracking |
| JSON | API response format validated across <br>
<hr>

##  🧪 Testing Approach
### Functional Testing (Positive Cases)<br>
Validated correct API behavior for valid requests, including:<br>
📌 HTTP status codes (200 OK)<br>
📌 Accurate weather data retrieval<br>
📌 Proper JSON structure<br>

### 🔕 Negative & Edge Case Testing<br>
Tested how the API handles invalid or unexpected input:<br>

📌 Invalid or missing API key → 401 Unauthorized<br>
📌 Invalid location → 404 Not Found<br>
📌 Malformed parameters → 400 Bad Request<br>
📌 Empty requests → graceful failure handling<br>

### 📢 Response Validation<br>
Each API response was checked against expected values for:<br>

📌 HTTP status codes (e.g., 200 OK, 401 Unauthorized, 404 Not Found)<br>
📌 JSON response structure and required fields<br>
📌 Data accuracy and format compliance<br>
<hr>

### 📡 API Endpoint Tested<br>

GET http://dataservice.accuweather.com/currentconditions/v1/{locationKey}<br>

#### Query Parameters
| Parameter | Description | Data |
| :---     | :---  |  :--- |
| locationKey | AccuWeather location ID for the city | 4180439 (Atlanta) |
| details| Returns full weather details  | true |
| units |   Temperature unit  | imperial (°F), metric (°C) | 
| appid | API key (required) | {SECURE_API_KEY} |<br>

<hr>

#### 📊 Test Case Documentation<br>
Test cases were written and tracked in an Excel spreadsheet covering:<br>
<br>
📁 Test Description — What is being validated<br>
📁 Expected Result — Anticipated HTTP status code and response behavior<br>
📁 Test Details / How to Test - Parameters and Methods to obtain data<br>
✔️Pass / ❌Fail Status — Documented outcome for each test<br>

📝 Test cases provide clear guidance and direction on what to verify and how to conduct the checks.<br>
   Below is an example of a test case written for tracking results:<br>

![image](https://github.com/user-attachments/assets/a35de218-c312-46b6-9b30-51534ad2307f)


<hr>

#### 🔍 Test Scenarios Covered
| Scenario Type | Description | 
| :---     | :---  | 
| ✅ Valid city name| requestReturns 200 OK with full weather data|<br>
| ✅ Valid city ID | requestReturns 200 OK with location-matched data|<br>
| ✅ Imperial units | requestTemperature returned in Fahrenheit|<br>
| ✅ Metric units | requestTemperature returned in Celsius|
| ❌ Invalid API | keyReturns 401 Unauthorized|<br>
| ❌ Missing API | keyReturns 401 Unauthorized|<br>
| ❌ Invalid city name | Returns 404 Not Found|<br>
| ❌ Malformed request | parametersValidates error handling behavior|<br>
| ❌ Empty query string | Validates graceful failure response|<br>
<hr>


#### 📦 Sample Successful Response (200 OK)<br>

```json

{
  "coord": { "lon": -84.388, "lat": 33.749 },
  "weather": [{ "main": "Clouds", "description": "few clouds" }],
  "main": {
    "temp": 41.2,
    "feels_like": 35.6,
    "temp_min": 32.4,
    "temp_max": 47.0,
    "humidity": 65
  },
  "wind": { "speed": 8.1, "deg": 80 },
  "name": "Atlanta",
  "cod": 200
}
```
---
🚀 Postman API documentation link for the weather test calls. <br>
API DOCUMENTATION:
<br>
https://documenter.getpostman.com/view/31215339/2sAYJ9AJ9v
<hr>






