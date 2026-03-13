# Daily Weather Report Automation (n8n)

## Overview
This project is an automation workflow built with **n8n** that retrieves daily weather data from a weather API and automatically sends a summarized weather report via email every 24 hours.

The workflow demonstrates API integration, scheduling automation, data parsing, and email notification using n8n.

## Features
- Runs automatically every 24 hours
- Fetches weather data from a public Weather API
- Parses JSON weather data
- Formats a readable weather report
- Sends the report automatically via Gmail

## Workflow Architecture

Schedule Trigger → HTTP Request → Data Processing → Gmail Send Email

### 1. Schedule Trigger
- Triggers the workflow every 24 hours.
- Ensures the weather report is sent daily.

### 2. HTTP Request Node
- Sends a request to a weather API.
- Retrieves the latest weather data for the selected location.

Example API endpoint:
```

https://api.openweathermap.org/data/2.5/weather?q=City&appid=API_KEY

```

### 3. Data Processing
- Extracts relevant data from the API response such as:
  - Temperature
  - Weather condition
  - Humidity
  - Wind speed

- Formats the data into a readable message.

Example output:

```

Daily Weather Report

Location: Lagos
Temperature: 28°C
Condition: Clear Sky
Humidity: 70%
Wind Speed: 5 m/s

```

### 4. Gmail Node
- Sends the formatted weather report via email automatically.

## Technologies Used
- **n8n**
- REST APIs
- JSON Data Processing
- Gmail Integration

## Use Cases
- Daily weather alerts
- Automated reporting
- API data monitoring
- Email notification systems

## How to Use

1. Import the workflow JSON into n8n.
2. Add your Weather API key.
3. Connect your Gmail account.
4. Set the desired city/location.
5. Activate the workflow.

Once activated, the workflow will automatically send a weather report every 24 hours.

## Future Improvements
- Add multiple city monitoring
- Add weather alerts (rain/storm warnings)
- Store weather data in a database
- Send reports to Slack or Telegram

## Author
**Uhunoma Paul**

Automation Developer (n8n)
