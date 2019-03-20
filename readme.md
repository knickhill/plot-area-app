## Farm Area Calculator

A simple jupyter notebook based app to calculate area of a small polygonal plot.

Input: Geographic coordinates of the corners of the plot from Google Maps API <break/>
Returns: Area of the plot


## How it works

- Input address to display a google map centered around the chosen point
- Place markers to indicate lat, lng coordinates of the corners of the plot
- The polygonal area is converted to cartesian coordinates using the Universal Transverse Mercator projection. (This is not an equal area projection, but works for small areas)
- Compute area of projection in sq-m, acres, and feet

## Dependencies

Download and API key to use with GoogleMaps and save it in the root directory. For instructions on how to do this, visit https://developers.google.com/maps/documentation/javascript/get-api-key

Python packages:
gmaps
googlemaps python client
pyproj
shapely

It is a pain to install pyproj and shapely successfully using pip. Use conda with channel conda-forge instead.

## Future improvements

- Use the right projection
- Containerize the app on docker and host it on Heroku
- Write tests to validate that the area is accurate by measuring plots whose area is known
