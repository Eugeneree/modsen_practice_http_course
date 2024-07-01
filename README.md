1 http-request with GET method:
https://api.openweathermap.org/data/2.5/weather?q=Moscow&appid=b2f76331b4a22593fef4698d08cb1757

http-response with GET method:
{
    "coord": {
        "lon": 37.6156,
        "lat": 55.7522
    },
    "weather": [
        {
            "id": 804,
            "main": "Clouds",
            "description": "overcast clouds",
            "icon": "04d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 303.25,
        "feels_like": 302.84,
        "temp_min": 301.44,
        "temp_max": 303.9,
        "pressure": 1011,
        "humidity": 39,
        "sea_level": 1011,
        "grnd_level": 992
    },
    "visibility": 10000,
    "wind": {
        "speed": 3.21,
        "deg": 214,
        "gust": 3.76
    },
    "clouds": {
        "all": 99
    },
    "dt": 1719828476,
    "sys": {
        "type": 2,
        "id": 2094500,
        "country": "RU",
        "sunrise": 1719794994,
        "sunset": 1719857801
    },
    "timezone": 10800,
    "id": 524901,
    "name": "Moscow",
    "cod": 200
}

2 http-request with GET method:
https://api.openweathermap.org/data/2.5/weather?q=Mosco&appid=b2f76331b4a22593fef4698d08cb1757

http-response with GET method:
{
    "cod": "404",
    "message": "city not found"
}

3 http-request with GET method:
https://api.openweathermap.org/data/2.5/weather?q=Mosco&appid=b2f76331b4a22593fef4698d08cb175

http-response with GET method:

{
    "cod": 401,
    "message": "Invalid API key. Please see https://openweathermap.org/faq#error401 for more info."
}

4 http-request with POST method:
https://api.openweathermap.org/data/2.5/weather?q=Moscow&appid=b2f76331b4a22593fef4698d08cb1757

http-response with post method:
{
    "coord": {
        "lon": 37.6156,
        "lat": 55.7522
    },
    "weather": [
        {
            "id": 804,
            "main": "Clouds",
            "description": "overcast clouds",
            "icon": "04d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 302.43,
        "feels_like": 301.61,
        "temp_min": 301.44,
        "temp_max": 303.9,
        "pressure": 1010,
        "humidity": 35,
        "sea_level": 1010,
        "grnd_level": 992
    },
    "visibility": 10000,
    "wind": {
        "speed": 3.59,
        "deg": 226,
        "gust": 3.94
    },
    "clouds": {
        "all": 99
    },
    "dt": 1719829928,
    "sys": {
        "type": 2,
        "id": 2000314,
        "country": "RU",
        "sunrise": 1719794994,
        "sunset": 1719857801
    },
    "timezone": 10800,
    "id": 524901,
    "name": "Moscow",
    "cod": 200
}

Other http methods are not supported or not allowed by the OpenWeather API. They cause these responses:
{
    "cod": "405",
    "message": "Internal error"
}
