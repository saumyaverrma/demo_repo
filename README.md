# Exposure-Autocounter

Track your personal pollution exposure using this app which helps users understand how much polluted air they personally breathe every day using *live AQI data* and *geofencing*.

## Description
This app gives us:

### Real-Time AQI (Air Quality)
● AQI level near the user
<br>
● Pollutant concentration like PM2.5 <br>
● Real-time updates
### Outdoor Exposure Timer
● User sets home location <br>
● Geofence detects when user leaves/enters home <br>
● Exposure = Time Outside × AQI
### Daily Exposure Summary
Displays: <br>
● Today’s time outdoors <br>
● Average AQI <br>
● Total exposure score <br>
### AI Recovery Plan (New Feature)
● At the end of the day, the app generates: <br>
● 2–4 minute breathing exercise <br>
● Two diet/home remedy suggestions <br>
● Short safety disclaimer <br>
● Powered by Gemini API (one call per day) <br>

## How It Works
1.User sets home location → geofence created <br>
2.Leaving home → timer starts <br>
3.Entering home → timer stops <br>
4.Live AQI fetched periodically <br>
5.Exposure calculated: 
```
exposure = minutes_outside × average_aqi
```
6.App calls Gemini with user’s exposure summary <br>
7.Gemini returns structured JSON with breathing + diet plan

## Tech Stack
1.Flutter <br>
2.OpenAQ API for real-time AQI <br>
3.Gemini API for recovery plan generation <br>

## MVP Scope
1.Set home geofence <br>
2.Auto start/stop outdoor timer <br>
3.Fetch real-time AQI <br>
4.Exposure calculation <br>
5.Exposure summary UI <br>
6.AI-generated recovery plan screen <br>

## Installation
1.clone the project into your system
```
git clone <repo>
```
2.open project in Android Studio <br>
3.add Gemini API key <br>
4.run on device <br>


