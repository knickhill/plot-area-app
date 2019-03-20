## Farm Area Calculator

A simple jupyter notebook based app to calculate area of a small polygonal plot.

Input: Geographic coordinates of the corners of the plot from Google Maps API
Returns: Area of the plot


## How it works

- Entering address of center of polygon displays google map centered around it
- Place markers on corners of the plot. The app reads the markers as lat, lng coordinates
- The polygonal area is converted to cartesian coordinates by projecting it using Universal Transverse Mercator system. (This is not an equal area projection, but works for small areas. Will correct this in future)
- Compute area of projection in sq-m, acres, and feet

## Dependencies

Download and API key to use with GoogleMaps and save it in the same directory. For instructions, visit https://developers.google.com/maps/documentation/javascript/get-api-key

Python packages used:
gmaps
googlemaps python client
pyproj
shapely

## Future improvements

- Use the right projection
- Containerize the app on docker and host it on Heroku
- Write tests to validate that the area is accurate by measuring plots whose area is known
