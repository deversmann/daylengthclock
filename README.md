# Day Length Clock

A browser-based visualization tool that displays the current progression through daylight and nighttime hours based on your geographic location.

## Overview

Day Length Clock is a simple web application that uses geolocation and sunrise/sunset data to create an intuitive visual representation of where you are in the current day/night cycle. The clock calculates and displays the percentage of daylight elapsed, nighttime elapsed, and overall day completion.

## Project Description

This project provides multiple variations of a day length visualization clock. Using the browser's geolocation API and the Sunrise-Sunset API, it dynamically calculates solar events for your location and presents them in an easy-to-understand graphical format.

### Key Features

- **Automatic Location Detection**: Uses browser geolocation API to determine your latitude and longitude
- **Real-time Sunrise/Sunset Data**: Fetches current solar event times from api.sunrisesunset.io
- **Visual Progress Indicators**: Displays percentage-based progress bars for daylight and day completion
- **Multiple Visualizations**: Includes different UI variations with varying levels of detail
- **Auto-refresh**: Updates data every 5 minutes to maintain accuracy
- **No Backend Required**: Pure client-side JavaScript application

## Technical Stack

- **HTML5**: Semantic markup with geolocation API integration
- **CSS3**: Custom styling with W3.CSS framework (clock.html variant)
- **Vanilla JavaScript**: XMLHttpRequest for API calls, DOM manipulation
- **External APIs**:
  - Sunrise-Sunset API (api.sunrisesunset.io) for solar event data
  - Font Awesome for iconography
  - W3.CSS for theming (in some variants)

## File Structure

```
daylengthclock/
├── index.html          # Simple day length clock with basic styling
├── clock.html          # More detailed visualization with separate day/night tracking
├── clock2.html         # Alternative visualization variant
├── temp.json           # Sample API response data
├── temp2.json          # Sample API response data
├── temp3.json          # Sample API response data
├── temp4.html          # Development/testing file
├── temp5.json          # Sample API response data
├── LICENSE             # MIT License
└── README.md           # This file
```

## Available Versions

### index.html
The simplest implementation featuring:
- Single progress bar showing day completion percentage
- Split header showing sun/moon icons with proportional width based on day length
- Minimal styling with dark theme
- Updates every 5 minutes

### clock.html
Enhanced version with:
- W3.CSS theming framework
- Separate tracking of daytime elapsed vs nighttime elapsed percentages
- Tooltips showing exact percentages
- Visual separation of day and night sections
- More polished UI with rounded corners and shadows
- Debug output panel for development
- Mobile-responsive design

### clock2.html
Third visualization variant (content similar to above implementations)

## How It Works

1. **Geolocation Request**: On page load, requests user's current position
2. **API Call**: Sends latitude/longitude to Sunrise-Sunset API
3. **Data Processing**: Calculates:
   - Day length as percentage of 24 hours
   - Current position in the full day (0-100%)
   - Current position within daylight hours (0-100% if before sunset)
   - Current position within nighttime hours (0-100% if after sunset)
4. **Visual Update**: Renders progress bars and percentages
5. **Periodic Refresh**: Re-fetches data every 5 minutes

## Usage

Simply open any of the HTML files in a modern web browser:

1. Browser will request location permission
2. Grant permission to enable the clock
3. Clock will automatically display and update

No build process, dependencies, or server required.

## Limitations

- **Requires Geolocation**: Will not function if location permission is denied
- **Internet Required**: Needs active connection to fetch sunrise/sunset data
- **Browser Support**: Requires modern browser with geolocation API support
- **Accuracy**: Updates every 5 minutes; not second-precise

## Current State

**Status**: Experimental/Proof-of-concept  
**Last Updated**: April 2026  
**Activity**: Single initial commit with multiple visualization experiments  
**Completeness**: Functional but contains temp files and development artifacts

This appears to be an active exploration of different ways to visualize day length data. The project contains multiple working implementations alongside test data files, suggesting ongoing experimentation with the best presentation format. All core functionality is operational, but the repository could benefit from cleanup of temporary files.

## Potential Enhancements

- Remove temporary JSON and HTML files once final design is chosen
- Add timezone handling for more accurate calculations
- Include sunrise/sunset times in the display
- Add location name display
- Create configuration options (refresh interval, units, theme)
- Add error handling for API failures or offline scenarios
- Include weekly/monthly day length trends

---

*This README was auto-generated by Claude on April 10, 2026.*
