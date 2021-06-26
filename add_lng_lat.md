```python
pip install googlemaps
pip install folium
```

    Requirement already satisfied: googlemaps in ./opt/anaconda3/lib/python3.8/site-packages (4.4.2)
    Requirement already satisfied: requests<3.0,>=2.20.0 in ./opt/anaconda3/lib/python3.8/site-packages (from googlemaps) (2.24.0)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (1.25.9)
    Requirement already satisfied: certifi>=2017.4.17 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (2020.6.20)
    Requirement already satisfied: chardet<4,>=3.0.2 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (3.0.4)
    Requirement already satisfied: idna<3,>=2.5 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (2.10)
    Note: you may need to restart the kernel to use updated packages.



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

    127.4011048 36.44288299999999
    대한민국 대전광역시 대덕구 목상동 문평서로 8-24

