# 🌦️ Go Weather API

A simple REST API built with Go that fetches real-time weather information for any city using the OpenWeatherMap API.

## Features

- Fetch current weather by city name
- RESTful API
- JSON response
- Lightweight and fast
- Easy to configure using an API key

---

## Technologies Used

- Go (Golang)
- net/http
- encoding/json
- OpenWeatherMap API

---

## Project Structure

```
.
├── main.go
├── go.mod
├── .apiConfig
└── README.md
```

---

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/devyanshigoswami/go-weather-api.git
cd go-weather-api
```

### 2. Install Go

Download Go from:

https://go.dev/dl/

Verify installation:

```bash
go version
```

### 3. Get an OpenWeatherMap API Key

Create a free account at:

https://openweathermap.org/api

Copy your API key.

### 4. Create `.apiConfig`

Create a file named `.apiConfig` in the project root.

Example:

```json
{
    "OpenWeatherMapApiKey": "YOUR_API_KEY"
}
```

---

## Run the Application

```bash
go run main.go
```

The server starts on:

```
http://localhost:8080
```

---

## API Endpoints

### Health Check

```
GET /hello
```

Example:

```
http://localhost:8080/hello
```

Response

```
hello from go!
```

---

### Get Weather

```
GET /weather/{city}
```

Example

```
http://localhost:8080/weather/London
```

Example Response

```json
{
  "name": "London",
  "main": {
    "temp": 294.52
  }
}
```

---

## How It Works

1. The user sends a city name.
2. The API reads the OpenWeatherMap API key from `.apiConfig`.
3. A request is sent to the OpenWeatherMap API.
4. The weather data is received.
5. The API returns the weather data in JSON format.


---

Screenshot:
<img width="522" height="148" alt="image" src="https://github.com/user-attachments/assets/38e2034e-85c6-4653-949d-7cc381dd5551" />

