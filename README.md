# Nimbus Vista

Nimbus Vista is a modern, animated weather web app that shows real-time conditions and a 5-day forecast for any searched location.

<img width="1910" height="1165" alt="image1" src="https://github.com/user-attachments/assets/fac21aa4-787e-4113-8494-f18f15f7fba6" />
<img width="1910" height="1165" alt="image2" src="https://github.com/user-attachments/assets/9a04d0c1-d293-4fb2-8b64-518c69123ef1" />


## Features
- Search weather by city or place name
- Auto-detect user location with browser geolocation
- Real-time current weather summary
- 5-day outlook with condition-based animated icons
- Clean, responsive glassmorphism-style UI
- Country and location badges for context

## Technologies Used

### Core Frontend
- **HTML5**: Application structure and semantic layout
- **CSS3**: Custom styling, responsive layout, gradients, and glassmorphism effects
- **Vanilla JavaScript (ES6+)**: App logic, API calls, rendering, and event handling

### Browser APIs
- **Geolocation API**: Detects user coordinates (with permission) for default weather loading
- **Fetch API**: Performs asynchronous HTTP requests to external weather/geocoding services

### External APIs
- **Open-Meteo API** (`api.open-meteo.com`)
  - Current weather and daily forecast data
  - No API key required
- **Nominatim (OpenStreetMap) API** (`nominatim.openstreetmap.org`)
  - Forward geocoding (place name -> latitude/longitude)
  - Reverse geocoding (latitude/longitude -> city/country)

### UI Libraries / Assets
- **Font Awesome 6** (CDN): Weather and interface icons
- **Google Fonts (Inter)**: Typography

## Project Structure
```text
.
|- index.html      # Main page markup and external asset links
|- style.css       # Full visual styling and responsive design
|- script.js       # Weather logic, API integration, and dynamic rendering
```

## How It Works
1. On load, the app attempts geolocation to fetch local weather.
2. Coordinates are reverse-geocoded to resolve city/country labels.
3. Weather data is fetched from Open-Meteo.
4. WMO weather codes are mapped into human-readable conditions.
5. UI is rendered dynamically with animated condition icons.
6. Users can search any city/place to refresh data.

## Run Locally
1. Download or clone this project.
2. Open `index.html` in a browser.

No build tools or package installation are required.

## Notes
- Internet access is required for live API responses.
- Geolocation permission improves default weather accuracy.
- Pressure and some derived values are approximated in current implementation.

## Future Improvements
- Add temperature unit toggle (C/F)
- Add hourly forecast section
- Better error handling and retries for API failures
- Optional backend proxy for request control and caching

---
Built as a lightweight frontend weather experience with modern visual design and live global data.
