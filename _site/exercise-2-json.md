# JSON exercise 2

## Step 1

JSON data

```json
{
 "date": "2015-09-01",
  "description": "sunny",
  "maxTemp": 22,
  "minTemp": 20,
  "windSpeed": 12,
  "danger": false
}
```

Represents a one-day weather forecast

Element | Description | Type | Notes
---- | ---- | ---- | ----
date | Date of forecast | string |
description | Description of weather | string | Values: "sunny", "overcast", "partly cloudy", "raining", and "snowing"
maxTemp | Maximum temperature | integer | Expressed in degrees Celsius
minTemp | Minimum temperature | integer | Expressed in degrees Celsius
windSpeed | Wind speed | integer | Kilometers per hour
danger | True if the weather conditions are dangerous; otherwise, false | Boolean |

## Step 2

JSON data

```json
 "longitude": 47.60,
 "latitude": 122.33,
 "forecasts": [
 {
 "date": "2015-09-01",
 "description": "sunny",
 "maxTemp": 22,
 "minTemp": 20,
 "windSpeed": 12,
   "danger": false
 },
 {
 "date": "2015-09-02",
 "description": "overcast",
 "maxTemp": 21,
 "minTemp": 17,
 "windSpeed": 15,
   "danger": false
 },
 {
 "date": "2015-09-03",
 "description": "raining",
 "maxTemp": 20,
 "minTemp": 18,
 "windSpeed": 13,
   "danger": false
 }
 ]
}
```
Represents a multiple-day weather forecast

Element | Description | Type | Notes
---- | ---- | ---- | ----
longitude | Longitude of location | decimal |
latitude | Latitude of location | decimal |
forecasts | Forecast data object | array of daily forecast objects |
`date` | Date of forecast | string | Format is YYYY-MM-DD
`description` | Description of weather | string | Values: "sunny", "overcast", "partly cloudy", "raining", and "snowing"
`maxTemp` | Maximum temperature | integer | Expressed in degrees Celsius
`minTemp` | Minimum temperature | integer | Expressed in degrees Celsius
`windSpeed` | Wind speed | integer | Kilometers per hour
`danger` | Shows whether the weather is dangerous | Boolean |

## Step 3

JSON data

```json
{
 "meeting" : {
 "time": "2015-09-01 10:00",
 "duration": 60,
   "description": "2016 Strategic Planning Meeting",
   "location": "Building 23, Room 206",
   "reminder": 15,
   "invitees": ["michael@example.com", "thelma@example.com",
 "david@example.com", "leon@example.com"]
  }
}
```

Request data to create a new meeting for the online calendar

Element | Description | Type | Required | Notes
---- | ---- | ---- | ---- | ----
meeting | Object with meeting information | Object | Required |
time | Start time of meeting (GMT) | string | Required | Format is YYYY-MM-DD HH:MM
duration | Duration of meeting in minutes | number | Required |
description | Description of event | string | Required |
location | Location of the event | string | Optional | Default is an empty string
reminder | Number of minutes before event to send a reminder | number | Optional | Default is 10 minutes
invitees | Number of people to invite | array of strings | Default is an empty array |
