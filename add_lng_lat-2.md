```python
pip install googlemaps
pip install folium
```


```python
import folium
import pandas as pd
import googlemaps
import numpy as np
```


```python
gmaps_key ='AIzaSyB7Lq1eQOfGMZuzKYBw9EnPQf1eq0GkQ0I'
gmaps = googlemaps.Client(key=gmaps_key)
```


```python
geocode_result = gmaps.geocode(('레딕스'), language = 'ko')
#print(geocode_result[0])
```


```python
location_out = geocode_result[0].get('geometry')
print(location_out['location']['lng'],location_out['location']['lat'])
location_out = geocode_result[0].get('formatted_address')
print(location_out)
```
