# WeatherAppPython
Python Dependencies Installation Guide
This repository contains code that relies on several Python libraries. Here's a guide to help you install them:

Dependencies
Geopy: A Python library to locate the coordinates of addresses, cities, countries, and landmarks across the globe using third-party geocoders and other data sources.
Pytz: World timezone definitions, modern and historical.
Timezonefinder: A Python library to quickly find the timezone of any given location on Earth.
Requests: A simple HTTP library for Python, built for human beings.
Installation Guide
You can install these dependencies using pip, Python's package installer. If you don't have pip installed, you can follow the official documentation to install it.

Open your terminal or command prompt and run the following commands:

bash
Copy code
pip install geopy
pip install pytz
pip install timezonefinder
pip install requests
Usage
Once you have installed these dependencies, you can use them in your Python scripts by importing them at the beginning of your code:

python
Copy code
from geopy.geocoders import Nominatim
import pytz
from timezonefinder import TimezoneFinder
import requests
Example
Here's a simple example demonstrating how to use these libraries together:

python
Copy code
from geopy.geocoders import Nominatim
import pytz
from timezonefinder import TimezoneFinder
import requests

# Example usage of Geopy
geolocator = Nominatim(user_agent="geoapiExercises")
location = geolocator.geocode("175 5th Avenue NYC")
print("Latitude and Longitude of the said address:")
print((location.latitude, location.longitude))

# Example usage of Pytz
tz = pytz.timezone('America/New_York')
print("Timezone:", tz)

# Example usage of Timezonefinder
tf = TimezoneFinder()
timezone = tf.timezone_at(lat=40.7128, lng=-74.0060)
print("Timezone of given coordinates:", timezone)

