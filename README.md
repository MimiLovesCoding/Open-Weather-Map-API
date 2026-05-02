# ⛅ 🌈 Open-Weather-Map-API—Comprehensive API Test Suite☀️☔

<hr>

A full-cycle API validation project using Postman and the OpenWeatherMap API, covering functional testing, negative/edge case testing, response validation, and structured test case documentation.

🔐 API keys, request headers, and body parameters have been omitted from all documentation for security purposes.

<hr>

##  📋 Project Overview <br>
This project validates the reliability, accuracy, and robustness of the OpenWeatherMap API endpoints through a structured test suite. Testing included both positive scenarios (verifying expected behavior) and negative/stress scenarios (intentionally attempting to break the API to identify vulnerabilities and failure handling).
The API was confirmed to be robust, well-designed, and compliant with expected standards across all tested scenarios.<br>
<hr>

## 🛠 Tools & Technologies <br>
| Tools | Purpose |
| :---: | :---: |
| [ Postman](https://postman.com) | API client for building, executing, and documenting test calls |
|[Accuweather API](https://developer.accuweather.com/core-weather/location-key-currentconditions) | Third-party REST API providing real-time global weather data |
| Microsoft Excel |Structured test case management and results tracking |
| JSON | API response format validated across <br>
<hr>

##  🧪 Testing Approach
### Functional Testing (Positive Cases)<br>
Verified that valid API requests returned correct HTTP status codes, accurate weather data, and properly structured JSON responses.<br>

### 🔕 Negative & Edge Case Testing<br>
Intentionally submitted invalid, malformed, and unauthorized requests to validate that the API handles failures gracefully and returns appropriate error responses.<br>

### 📢 Response Validation<br>
Each API response was checked against expected values for:

📌 HTTP status codes (e.g., 200 OK, 401 Unauthorized, 404 Not Found)<br>
📌 JSON response structure and required fields<br>
📌 Data accuracy and format compliance<br>

<hr>
📝 Test cases provide clear guidance and direction on what to verify and how to conduct the checks. Below is a snippet from the attached Excel spreadsheet.

![image](https://github.com/user-attachments/assets/a35de218-c312-46b6-9b30-51534ad2307f)


<hr>

🚀 Postman API documentation link for the weather test calls. <br>
API DOCUMENTATION:
<br>
https://documenter.getpostman.com/view/31215339/2sAYJ9AJ9v

