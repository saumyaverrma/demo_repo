# Exposure-Autocounter

Track your personal pollution exposure using this app which helps users understand how much polluted air they personally breathe every day using *live AQI data* and *geofencing*.

## Description
This app gives us:

### Real-Time AQI (Air Quality)
● AQI level near the user
<br>
● Pollutant concentration like PM2.5
● Real-time updates
### Outdoor Exposure Timer
● User sets home location
● Geofence detects when user leaves/enters home
● Exposure = Time Outside × AQI
### Daily Exposure Summary
Displays:
● Today’s time outdoors
● Average AQI
● Total exposure score
### AI Recovery Plan (New Feature)
● At the end of the day, the app generates:
● 2–4 minute breathing exercise
● Two diet/home remedy suggestions
● Short safety disclaimer
● Powered by Gemini API (one call per day)

## How It Works
1.User sets home location → geofence created
2.Leaving home → timer starts
3.Entering home → timer stops
4.Live AQI fetched periodically
5.Exposure calculated:
```
exposure = minutes_outside × average_aqi
```
6.App calls Gemini with user’s exposure summary
7.Gemini returns structured JSON with breathing + diet plan

## Tech Stack
1.Flutter 
2.OpenAQ API for real-time AQI
3.Gemini API for recovery plan generation

## MVP Scope
1.Set home geofence
2.Auto start/stop outdoor timer
3.Fetch real-time AQI
4.Exposure calculation
5.Exposure summary UI
6.AI-generated recovery plan screen

## Installation
1.git clone <repo>
2.open project in Android Studio
3.add Gemini API key
4.run on device


