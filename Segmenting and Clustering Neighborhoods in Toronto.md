<h1> QUESTION 1</H1>

<H1>1. Notebook book created</H1>


```python
import numpy as np # library to handle data in a vectorized manner
import pandas as pd # library for data analsysis
import requests # Library for web scraping

print('Libraries imported.')
```

    Libraries imported.



```python
conda install -c anaconda beautifulsoup4
```

    Solving environment: done
    
    
    ==> WARNING: A newer version of conda exists. <==
      current version: 4.5.11
      latest version: 4.8.0
    
    Please update conda by running
    
        $ conda update -n base -c defaults conda
    
    
    
    # All requested packages already installed.
    
    
    Note: you may need to restart the kernel to use updated packages.



```python
 conda update -n base -c defaults conda
```

    Solving environment: done
    
    ## Package Plan ##
    
      environment location: /home/jupyterlab/conda
    
      added / updated specs: 
        - conda
    
    
    The following packages will be downloaded:
    
        package                    |            build
        ---------------------------|-----------------
        six-1.13.0                 |           py38_0          27 KB
        pyopenssl-19.1.0           |           py38_0          87 KB
        pysocks-1.7.1              |           py38_0          27 KB
        python-3.8.0               |       h0371630_2        39.6 MB
        wheel-0.33.6               |           py38_0          35 KB
        ncurses-6.1                |       he6710b0_1         958 KB
        pip-19.3.1                 |           py38_0         1.9 MB
        ruamel_yaml-0.15.87        |   py38h7b6447c_0         269 KB
        requests-2.22.0            |           py38_1          90 KB
        setuptools-42.0.2          |           py38_0         654 KB
        pycosat-0.6.3              |   py38h7b6447c_0         113 KB
        conda-package-handling-1.6.0|   py38h7b6447c_0         879 KB
        tqdm-4.40.2                |             py_0          53 KB
        zlib-1.2.11                |       h7b6447c_3         120 KB
        libedit-3.1.20181209       |       hc058e9b_0         188 KB
        sqlite-3.30.1              |       h7b6447c_0         1.9 MB
        urllib3-1.25.7             |           py38_0         161 KB
        certifi-2019.11.28         |           py38_0         156 KB
        openssl-1.1.1d             |       h7b6447c_3         3.7 MB
        cffi-1.13.2                |   py38h2e261b9_0         233 KB
        pycparser-2.19             |             py_0          89 KB
        asn1crypto-1.2.0           |           py38_0         159 KB
        conda-4.8.0                |           py38_1         3.0 MB
        idna-2.8                   |        py38_1000         103 KB
        cryptography-2.8           |   py38h1ba5d50_0         618 KB
        ca-certificates-2019.11.27 |                0         132 KB
        chardet-3.0.4              |        py38_1003         170 KB
        ------------------------------------------------------------
                                               Total:        55.4 MB
    
    The following NEW packages will be INSTALLED:
    
        _libgcc_mutex:          0.1-main               
        conda-package-handling: 1.6.0-py38h7b6447c_0   
    
    The following packages will be UPDATED:
    
        asn1crypto:             0.24.0-py37_0           --> 1.2.0-py38_0           
        ca-certificates:        2018.03.07-0            --> 2019.11.27-0           
        certifi:                2018.8.24-py37_1        --> 2019.11.28-py38_0      
        cffi:                   1.11.5-py37he75722e_1   --> 1.13.2-py38h2e261b9_0  
        chardet:                3.0.4-py37_1            --> 3.0.4-py38_1003        
        conda:                  4.5.11-py37_0           --> 4.8.0-py38_1           
        cryptography:           2.3.1-py37hc365091_0    --> 2.8-py38h1ba5d50_0     
        idna:                   2.7-py37_0              --> 2.8-py38_1000          
        libedit:                3.1.20170329-h6b74fdf_2 --> 3.1.20181209-hc058e9b_0
        libgcc-ng:              8.2.0-hdf63c60_1        --> 9.1.0-hdf63c60_0       
        ncurses:                6.1-hf484d3e_0          --> 6.1-he6710b0_1         
        openssl:                1.0.2p-h14c3975_0       --> 1.1.1d-h7b6447c_3      
        pip:                    10.0.1-py37_0           --> 19.3.1-py38_0          
        pycosat:                0.6.3-py37h14c3975_0    --> 0.6.3-py38h7b6447c_0   
        pycparser:              2.18-py37_1             --> 2.19-py_0              
        pyopenssl:              18.0.0-py37_0           --> 19.1.0-py38_0          
        pysocks:                1.6.8-py37_0            --> 1.7.1-py38_0           
        python:                 3.7.0-hc3d631a_0        --> 3.8.0-h0371630_2       
        requests:               2.19.1-py37_0           --> 2.22.0-py38_1          
        ruamel_yaml:            0.15.46-py37h14c3975_0  --> 0.15.87-py38h7b6447c_0 
        setuptools:             40.2.0-py37_0           --> 42.0.2-py38_0          
        six:                    1.11.0-py37_1           --> 1.13.0-py38_0          
        sqlite:                 3.24.0-h84994c4_0       --> 3.30.1-h7b6447c_0      
        tqdm:                   4.26.0-py37h28b3542_0   --> 4.40.2-py_0            
        urllib3:                1.23-py37_0             --> 1.25.7-py38_0          
        wheel:                  0.31.1-py37_0           --> 0.33.6-py38_0          
        zlib:                   1.2.11-ha838bed_2       --> 1.2.11-h7b6447c_3      
    
    
    Downloading and Extracting Packages
    six-1.13.0           | 27 KB     | ##################################### | 100% 
    pyopenssl-19.1.0     | 87 KB     | ##################################### | 100% 
    pysocks-1.7.1        | 27 KB     | ##################################### | 100% 
    python-3.8.0         | 39.6 MB   | ##################################### | 100% 
    wheel-0.33.6         | 35 KB     | ##################################### | 100% 
    ncurses-6.1          | 958 KB    | ##################################### | 100% 
    pip-19.3.1           | 1.9 MB    | ##################################### | 100% 
    ruamel_yaml-0.15.87  | 269 KB    | ##################################### | 100% 
    requests-2.22.0      | 90 KB     | ##################################### | 100% 
    setuptools-42.0.2    | 654 KB    | ##################################### | 100% 
    pycosat-0.6.3        | 113 KB    | ##################################### | 100% 
    conda-package-handli | 879 KB    | ##################################### | 100% 
    tqdm-4.40.2          | 53 KB     | ##################################### | 100% 
    zlib-1.2.11          | 120 KB    | ##################################### | 100% 
    libedit-3.1.20181209 | 188 KB    | ##################################### | 100% 
    sqlite-3.30.1        | 1.9 MB    | ##################################### | 100% 
    urllib3-1.25.7       | 161 KB    | ##################################### | 100% 
    certifi-2019.11.28   | 156 KB    | ##################################### | 100% 
    openssl-1.1.1d       | 3.7 MB    | ##################################### | 100% 
    cffi-1.13.2          | 233 KB    | ##################################### | 100% 
    pycparser-2.19       | 89 KB     | ##################################### | 100% 
    asn1crypto-1.2.0     | 159 KB    | ##################################### | 100% 
    conda-4.8.0          | 3.0 MB    | ##################################### | 100% 
    idna-2.8             | 103 KB    | ##################################### | 100% 
    cryptography-2.8     | 618 KB    | ##################################### | 100% 
    ca-certificates-2019 | 132 KB    | ##################################### | 100% 
    chardet-3.0.4        | 170 KB    | ##################################### | 100% 
    Preparing transaction: done
    Verifying transaction: done
    Executing transaction: done
    
    Note: you may need to restart the kernel to use updated packages.


<H1> 2. Web page scraped</H1>


```python
import requests
from urllib.request import urlopen
from bs4 import BeautifulSoup
import ssl
import csv

print('BeautifulSoup  & csv imported.')
```

    BeautifulSoup  & csv imported.



```python
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE

print('SSL certificate errors ignored.')
```

    SSL certificate errors ignored.



```python
source = requests.get('https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M').text

soup = BeautifulSoup(source, 'html5lib')

#print(soup.prettify())
print('soup ready')
```

    soup ready



```python
table = soup.find('table',{'class':'wikitable sortable'})
#table

```


```python
table_rows = table.find_all('tr')

#table_rows
```


```python
data = []
for row in table_rows:
    data.append([t.text.strip() for t in row.find_all('td')])

df = pd.DataFrame(data, columns=['PostalCode', 'Borough', 'Neighbourhood'])
df = df[~df['PostalCode'].isnull()]  # to filter out bad rows

print(df.head(5))
print('***')
print(df.tail(5))
```

      PostalCode           Borough     Neighbourhood
    1        M1A      Not assigned      Not assigned
    2        M2A      Not assigned      Not assigned
    3        M3A        North York         Parkwoods
    4        M4A        North York  Victoria Village
    5        M5A  Downtown Toronto      Harbourfront
    ***
        PostalCode       Borough          Neighbourhood
    283        M8Z     Etobicoke              Mimico NW
    284        M8Z     Etobicoke     The Queensway West
    285        M8Z     Etobicoke  Royal York South West
    286        M8Z     Etobicoke         South of Bloor
    287        M9Z  Not assigned           Not assigned


<h1> 3. Data transformed into pandas dataframe></h1>


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 287 entries, 1 to 287
    Data columns (total 3 columns):
    PostalCode       287 non-null object
    Borough          287 non-null object
    Neighbourhood    287 non-null object
    dtypes: object(3)
    memory usage: 9.0+ KB



```python
df.shape
```




    (287, 3)



<H1> 4. Dataframe cleaned and notebook annotate</H1>


```python
import pandas
import requests
from bs4 import BeautifulSoup
website_text = requests.get('https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M').text
soup = BeautifulSoup(website_text,'html5lib')

table = soup.find('table',{'class':'wikitable sortable'})
table_rows = table.find_all('tr')

data = []
for row in table_rows:
    data.append([t.text.strip() for t in row.find_all('td')])

df = pandas.DataFrame(data, columns=['PostalCode', 'Borough', 'Neighbourhood'])
df = df[~df['PostalCode'].isnull()]  # to filter out bad rows

#df.head(15)
```


```python
df.drop(df[df['Borough']=="Not assigned"].index,axis=0, inplace=True)
#df.head()
```


```python
df1 = df.reset_index()
#df1.head()
```


```python
df1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 210 entries, 0 to 209
    Data columns (total 4 columns):
    index            210 non-null int64
    PostalCode       210 non-null object
    Borough          210 non-null object
    Neighbourhood    210 non-null object
    dtypes: int64(1), object(3)
    memory usage: 6.7+ KB



```python
df1.shape
```




    (210, 4)



<text>More than one neighborhood can exist in one postal code area, M5A is listed twice and has two neighborhoods Harbourfront and Regent Park. These two rows will be combined into one row with the neighborhoods separated with a comma using groupby, see:

https://pandas-docs.github.io/pandas-docs-travis/user_guide/groupby.html</test>


```python
df2= df1.groupby('PostalCode').agg(lambda x: ','.join(x))

df2.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
    <tr>
      <th>PostalCode</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>M1B</th>
      <td>Scarborough,Scarborough</td>
      <td>Rouge,Malvern</td>
    </tr>
    <tr>
      <th>M1C</th>
      <td>Scarborough,Scarborough,Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
    </tr>
    <tr>
      <th>M1E</th>
      <td>Scarborough,Scarborough,Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>M1G</th>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>M1H</th>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 103 entries, M1B to M9W
    Data columns (total 2 columns):
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    dtypes: object(2)
    memory usage: 2.4+ KB



```python
df2.shape
```




    (103, 2)




```python
df2.loc[df2['Neighbourhood']=="Not assigned",'Neighbourhood']=df2.loc[df2['Neighbourhood']=="Not assigned",'Borough']

df2.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
    <tr>
      <th>PostalCode</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>M1B</th>
      <td>Scarborough,Scarborough</td>
      <td>Rouge,Malvern</td>
    </tr>
    <tr>
      <th>M1C</th>
      <td>Scarborough,Scarborough,Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
    </tr>
    <tr>
      <th>M1E</th>
      <td>Scarborough,Scarborough,Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>M1G</th>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>M1H</th>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3 = df2.reset_index()
df3.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough,Scarborough</td>
      <td>Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough,Scarborough,Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough,Scarborough,Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3['Borough']= df3['Borough'].str.replace('nan|[{}\s]','').str.split(',').apply(set).str.join(',').str.strip(',').str.replace(",{2,}",",")
```


```python
df3.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 103 entries, 0 to 102
    Data columns (total 3 columns):
    PostalCode       103 non-null object
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    dtypes: object(3)
    memory usage: 2.5+ KB



```python
df3.shape
```




    (103, 3)



<H1> QUESTION 2 </H1>

<H1>1. Used the Geocoder Package to get the coordinates of a few neighborhoods</H1>


```python
pip install geopy
```

    Collecting geopy
    [?25l  Downloading https://files.pythonhosted.org/packages/80/93/d384479da0ead712bdaf697a8399c13a9a89bd856ada5a27d462fb45e47b/geopy-1.20.0-py2.py3-none-any.whl (100kB)
    [K     |████████████████████████████████| 102kB 12.4MB/s ta 0:00:01
    [?25hCollecting geographiclib<2,>=1.49 (from geopy)
      Downloading https://files.pythonhosted.org/packages/8b/62/26ec95a98ba64299163199e95ad1b0e34ad3f4e176e221c40245f211e425/geographiclib-1.50-py3-none-any.whl
    Installing collected packages: geographiclib, geopy
    Successfully installed geographiclib-1.50 geopy-1.20.0
    Note: you may need to restart the kernel to use updated packages.



```python
from  geopy.geocoders import Nominatim
geolocator = Nominatim()
city ="London"
country ="Uk"
loc = geolocator.geocode(city+','+ country)
print("latitude is :-" ,loc.latitude,"\nlongtitude is:-" ,loc.longitude)
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:2: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      


    latitude is :- 51.5073219 
    longtitude is:- -0.1276474



```python
from  geopy.geocoders import Nominatim
geolocator = Nominatim()
location = geolocator.geocode("Toronto, North York, Parkwoods")

print(location.address)
print('')
print((location.latitude, location.longitude))
print('')
print(location.raw)
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:2: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      


    Parkwoods Village Drive, Parkway East, Don Valley East, North York, Toronto, Ontario, M3A 2X2, Canada
    
    (43.7587999, -79.3201966)
    
    {'place_id': 112665056, 'licence': 'Data © OpenStreetMap contributors, ODbL 1.0. https://osm.org/copyright', 'osm_type': 'way', 'osm_id': 160406961, 'boundingbox': ['43.7576231', '43.761106', '-79.3239088', '-79.316215'], 'lat': '43.7587999', 'lon': '-79.3201966', 'display_name': 'Parkwoods Village Drive, Parkway East, Don Valley East, North York, Toronto, Ontario, M3A 2X2, Canada', 'class': 'highway', 'type': 'secondary', 'importance': 0.51}



```python
import pandas as pd
df3.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
import pandas as pd
df_geopy = pd.DataFrame({'PostalCode': ['M3A', 'M4A', 'M5A'],
                         'Borough': ['North York', 'North York', 'Downtown Toronto'],
                         'Neighbourhood': ['Parkwoods', 'Victoria Village', 'Harbourfront'],})

from geopy.geocoders import Nominatim
geolocator = Nominatim()
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:7: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      import sys



```python
df_geopy1 = df3
df_geopy1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>98</th>
      <td>M9N</td>
      <td>York</td>
      <td>Weston</td>
    </tr>
    <tr>
      <th>99</th>
      <td>M9P</td>
      <td>Etobicoke</td>
      <td>Westmount</td>
    </tr>
    <tr>
      <th>100</th>
      <td>M9R</td>
      <td>Etobicoke</td>
      <td>Kingsview Village,Martin Grove Gardens,Richvie...</td>
    </tr>
    <tr>
      <th>101</th>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens,Beaumond Heights,Humbergate,Jam...</td>
    </tr>
    <tr>
      <th>102</th>
      <td>M9W</td>
      <td>Etobicoke</td>
      <td>Northwest</td>
    </tr>
  </tbody>
</table>
<p>103 rows × 3 columns</p>
</div>




```python
from geopy.geocoders import Nominatim
geolocator = Nominatim()

df_geopy1['address'] = df3[['PostalCode', 'Borough', 'Neighbourhood']].apply(lambda x: ', '.join(x), axis=1 )
df_geopy1.head()
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:2: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B, Scarborough, Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C, Scarborough, Highland Creek,Rouge Hill,Po...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E, Scarborough, Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G, Scarborough, Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H, Scarborough, Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_geopy1 = df3
```


```python
df_geopy1.shape
```




    (103, 4)




```python
df_geopy1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 103 entries, 0 to 102
    Data columns (total 4 columns):
    PostalCode       103 non-null object
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    address          103 non-null object
    dtypes: object(4)
    memory usage: 3.3+ KB



```python
df_geopy1.drop(df_geopy1[df_geopy1['Borough']=="Notassigned"].index,axis=0, inplace=True)
df_geopy1
# code holds true up until i=102
df_geopy1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 103 entries, 0 to 102
    Data columns (total 4 columns):
    PostalCode       103 non-null object
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    address          103 non-null object
    dtypes: object(4)
    memory usage: 4.0+ KB



```python
df_geopy1.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B, Scarborough, Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C, Scarborough, Highland Creek,Rouge Hill,Po...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E, Scarborough, Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G, Scarborough, Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H, Scarborough, Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_geopy1.shape
```




    (103, 4)




```python
df_geopy1.to_csv('geopy1.csv')

```


```python
geolocator = Nominatim()
location = geolocator.geocode("M1G, Scarborough, Woburn")
print(location.address)
print((location.latitude, location.longitude))
print(location.raw)
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:1: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      """Entry point for launching an IPython kernel.


    Woburn, Scarborough—Guildwood, Scarborough, Toronto, Golden Horseshoe, Ontario, M1H 2A2, Canada
    (43.7598243, -79.2252908)
    {'place_id': 4972888, 'licence': 'Data © OpenStreetMap contributors, ODbL 1.0. https://osm.org/copyright', 'osm_type': 'node', 'osm_id': 558715617, 'boundingbox': ['43.7597743', '43.7598743', '-79.2253408', '-79.2252408'], 'lat': '43.7598243', 'lon': '-79.2252908', 'display_name': 'Woburn, Scarborough—Guildwood, Scarborough, Toronto, Golden Horseshoe, Ontario, M1H 2A2, Canada', 'class': 'place', 'type': 'neighbourhood', 'importance': 0.558803667479001}



```python
pip install geocoder
```

    Collecting geocoder
    [?25l  Downloading https://files.pythonhosted.org/packages/4f/6b/13166c909ad2f2d76b929a4227c952630ebaf0d729f6317eb09cbceccbab/geocoder-1.38.1-py2.py3-none-any.whl (98kB)
    [K     |████████████████████████████████| 102kB 13.0MB/s ta 0:00:01
    [?25hCollecting ratelim (from geocoder)
      Downloading https://files.pythonhosted.org/packages/f2/98/7e6d147fd16a10a5f821db6e25f192265d6ecca3d82957a4fdd592cad49c/ratelim-0.1.6-py2.py3-none-any.whl
    Requirement already satisfied: requests in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from geocoder) (2.22.0)
    Collecting future (from geocoder)
    [?25l  Downloading https://files.pythonhosted.org/packages/45/0b/38b06fd9b92dc2b68d58b75f900e97884c45bedd2ff83203d933cf5851c9/future-0.18.2.tar.gz (829kB)
    [K     |████████████████████████████████| 829kB 7.2MB/s eta 0:00:01
    [?25hRequirement already satisfied: six in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from geocoder) (1.13.0)
    Collecting click (from geocoder)
    [?25l  Downloading https://files.pythonhosted.org/packages/fa/37/45185cb5abbc30d7257104c434fe0b07e5a195a6847506c074527aa599ec/Click-7.0-py2.py3-none-any.whl (81kB)
    [K     |████████████████████████████████| 81kB 17.3MB/s eta 0:00:01
    [?25hRequirement already satisfied: decorator in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from ratelim->geocoder) (4.4.1)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from requests->geocoder) (1.25.7)
    Requirement already satisfied: chardet<3.1.0,>=3.0.2 in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from requests->geocoder) (3.0.4)
    Requirement already satisfied: idna<2.9,>=2.5 in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from requests->geocoder) (2.8)
    Requirement already satisfied: certifi>=2017.4.17 in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from requests->geocoder) (2019.11.28)
    Building wheels for collected packages: future
      Building wheel for future (setup.py) ... [?25ldone
    [?25h  Stored in directory: /home/jupyterlab/.cache/pip/wheels/8b/99/a0/81daf51dcd359a9377b110a8a886b3895921802d2fc1b2397e
    Successfully built future
    Installing collected packages: ratelim, future, click, geocoder
    Successfully installed click-7.0 future-0.18.2 geocoder-1.38.1 ratelim-0.1.6
    Note: you may need to restart the kernel to use updated packages.



```python
df3.to_csv('geopy.csv')
```


```python
import csv

with open('geopy.csv') as csvfile:
     reader = csv.DictReader(csvfile)
     for row in reader:
         print(row['PostalCode'],row['Borough'], row['Neighbourhood'] )
```

    M1B Scarborough Rouge,Malvern
    M1C Scarborough Highland Creek,Rouge Hill,Port Union
    M1E Scarborough Guildwood,Morningside,West Hill
    M1G Scarborough Woburn
    M1H Scarborough Cedarbrae
    M1J Scarborough Scarborough Village
    M1K Scarborough East Birchmount Park,Ionview,Kennedy Park
    M1L Scarborough Clairlea,Golden Mile,Oakridge
    M1M Scarborough Cliffcrest,Cliffside,Scarborough Village West
    M1N Scarborough Birch Cliff,Cliffside West
    M1P Scarborough Dorset Park,Scarborough Town Centre,Wexford Heights
    M1R Scarborough Maryvale,Wexford
    M1S Scarborough Agincourt
    M1T Scarborough Clarks Corners,Sullivan,Tam O'Shanter
    M1V Scarborough Agincourt North,L'Amoreaux East,Milliken,Steeles East
    M1W Scarborough L'Amoreaux West
    M1X Scarborough Upper Rouge
    M2H NorthYork Hillcrest Village
    M2J NorthYork Fairview,Henry Farm,Oriole
    M2K NorthYork Bayview Village
    M2L NorthYork Silver Hills,York Mills
    M2M NorthYork Newtonbrook,Willowdale
    M2N NorthYork Willowdale South
    M2P NorthYork York Mills West
    M2R NorthYork Willowdale West
    M3A NorthYork Parkwoods
    M3B NorthYork Don Mills North
    M3C NorthYork Flemingdon Park,Don Mills South
    M3H NorthYork Bathurst Manor,Downsview North,Wilson Heights
    M3J NorthYork Northwood Park,York University
    M3K NorthYork CFB Toronto,Downsview East
    M3L NorthYork Downsview West
    M3M NorthYork Downsview Central
    M3N NorthYork Downsview Northwest
    M4A NorthYork Victoria Village
    M4B EastYork Woodbine Gardens,Parkview Hill
    M4C EastYork Woodbine Heights
    M4E EastToronto The Beaches
    M4G EastYork Leaside
    M4H EastYork Thorncliffe Park
    M4J EastYork East Toronto
    M4K EastToronto The Danforth West,Riverdale
    M4L EastToronto The Beaches West,India Bazaar
    M4M EastToronto Studio District
    M4N CentralToronto Lawrence Park
    M4P CentralToronto Davisville North
    M4R CentralToronto North Toronto West
    M4S CentralToronto Davisville
    M4T CentralToronto Moore Park,Summerhill East
    M4V CentralToronto Deer Park,Forest Hill SE,Rathnelly,South Hill,Summerhill West
    M4W DowntownToronto Rosedale
    M4X DowntownToronto Cabbagetown,St. James Town
    M4Y DowntownToronto Church and Wellesley
    M5A DowntownToronto Harbourfront
    M5B DowntownToronto Ryerson,Garden District
    M5C DowntownToronto St. James Town
    M5E DowntownToronto Berczy Park
    M5G DowntownToronto Central Bay Street
    M5H DowntownToronto Adelaide,King,Richmond
    M5J DowntownToronto Harbourfront East,Toronto Islands,Union Station
    M5K DowntownToronto Design Exchange,Toronto Dominion Centre
    M5L DowntownToronto Commerce Court,Victoria Hotel
    M5M NorthYork Bedford Park,Lawrence Manor East
    M5N CentralToronto Roselawn
    M5P CentralToronto Forest Hill North,Forest Hill West
    M5R CentralToronto The Annex,North Midtown,Yorkville
    M5S DowntownToronto Harbord,University of Toronto
    M5T DowntownToronto Chinatown,Grange Park,Kensington Market
    M5V DowntownToronto CN Tower,Bathurst Quay,Island airport,Harbourfront West,King and Spadina,Railway Lands,South Niagara
    M5W DowntownToronto Stn A PO Boxes 25 The Esplanade
    M5X DowntownToronto First Canadian Place,Underground city
    M6A NorthYork Lawrence Heights,Lawrence Manor
    M6B NorthYork Glencairn
    M6C York Humewood-Cedarvale
    M6E York Caledonia-Fairbanks
    M6G DowntownToronto Christie
    M6H WestToronto Dovercourt Village,Dufferin
    M6J WestToronto Little Portugal,Trinity
    M6K WestToronto Brockton,Exhibition Place,Parkdale Village
    M6L NorthYork Downsview,North Park,Upwood Park
    M6M York Del Ray,Keelesdale,Mount Dennis,Silverthorn
    M6N York The Junction North,Runnymede
    M6P WestToronto High Park,The Junction South
    M6R WestToronto Parkdale,Roncesvalles
    M6S WestToronto Runnymede,Swansea
    M7A Queen'sPark Queen's Park
    M7R Mississauga Canada Post Gateway Processing Centre
    M7Y EastToronto Business Reply Mail Processing Centre 969 Eastern
    M8V Etobicoke Humber Bay Shores,Mimico South,New Toronto
    M8W Etobicoke Alderwood,Long Branch
    M8X Etobicoke The Kingsway,Montgomery Road,Old Mill North
    M8Y Etobicoke Humber Bay,King's Mill Park,Kingsway Park South East,Mimico NE,Old Mill South,The Queensway East,Royal York South East,Sunnylea
    M8Z Etobicoke Kingsway Park South West,Mimico NW,The Queensway West,Royal York South West,South of Bloor
    M9A DowntownToronto Queen's Park
    M9B Etobicoke Cloverdale,Islington,Martin Grove,Princess Gardens,West Deane Park
    M9C Etobicoke Bloordale Gardens,Eringate,Markland Wood,Old Burnhamthorpe
    M9L NorthYork Humber Summit
    M9M NorthYork Emery,Humberlea
    M9N York Weston
    M9P Etobicoke Westmount
    M9R Etobicoke Kingsview Village,Martin Grove Gardens,Richview Gardens,St. Phillips
    M9V Etobicoke Albion Gardens,Beaumond Heights,Humbergate,Jamestown,Mount Olive,Silverstone,South Steeles,Thistletown
    M9W Etobicoke Northwest



```python
from  geopy.geocoders import Nominatim
geolocator = Nominatim()
location = geolocator.geocode("M1B Scarborough Rouge,Malvern")
print(location.address)
print((location.latitude, location.longitude))
print(location.raw)
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:2: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      


    Malvern, Scarborough—Rouge Park, Scarborough, Toronto, Golden Horseshoe, Ontario, M1B 4Y7, Canada
    (43.8091955, -79.2217008)
    {'place_id': 4979177, 'licence': 'Data © OpenStreetMap contributors, ODbL 1.0. https://osm.org/copyright', 'osm_type': 'node', 'osm_id': 558715616, 'boundingbox': ['43.8091455', '43.8092455', '-79.2217508', '-79.2216508'], 'lat': '43.8091955', 'lon': '-79.2217008', 'display_name': 'Malvern, Scarborough—Rouge Park, Scarborough, Toronto, Golden Horseshoe, Ontario, M1B 4Y7, Canada', 'class': 'place', 'type': 'neighbourhood', 'importance': 0.769448365439565}



```python
from  geopy.geocoders import Nominatim
geolocator = Nominatim()
location = geolocator.geocode("Toronto, Highland Creek")
print(location.address)
print((location.latitude, location.longitude))
print(location.raw)

```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:2: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      


    Highland Creek, Scarborough—Rouge Park, Scarborough, Toronto, Golden Horseshoe, Ontario, M1C 3T7, Canada
    (43.7901172, -79.1733344)
    {'place_id': 332533, 'licence': 'Data © OpenStreetMap contributors, ODbL 1.0. https://osm.org/copyright', 'osm_type': 'node', 'osm_id': 139354747, 'boundingbox': ['43.7900672', '43.7901672', '-79.1733844', '-79.1732844'], 'lat': '43.7901172', 'lon': '-79.1733344', 'display_name': 'Highland Creek, Scarborough—Rouge Park, Scarborough, Toronto, Golden Horseshoe, Ontario, M1C 3T7, Canada', 'class': 'place', 'type': 'neighbourhood', 'importance': 0.6480411950818731}



```python
from  geopy.geocoders import Nominatim
geolocator = Nominatim()
location = geolocator.geocode("Toronto, Morningside")
print(location.address)
print((location.latitude, location.longitude))
print(location.raw)
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:2: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      


    Morningside, Scarborough—Guildwood, Scarborough, Toronto, Golden Horseshoe, Ontario, M1G 3K5, Canada
    (43.7826012, -79.2049579)
    {'place_id': 332629, 'licence': 'Data © OpenStreetMap contributors, ODbL 1.0. https://osm.org/copyright', 'osm_type': 'node', 'osm_id': 139347757, 'boundingbox': ['43.7825512', '43.7826512', '-79.2050079', '-79.2049079'], 'lat': '43.7826012', 'lon': '-79.2049579', 'display_name': 'Morningside, Scarborough—Guildwood, Scarborough, Toronto, Golden Horseshoe, Ontario, M1G 3K5, Canada', 'class': 'place', 'type': 'neighbourhood', 'importance': 0.42000000000000004}


<H1>Retrieved coordinates with with lambda equation</H1>


```python
import pandas, os
os.listdir()
df_geopy=df3
df_geopy.head()
import geopy
dir(geopy)
type(df_geopy)
```




    pandas.core.frame.DataFrame




```python
df_geopy.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 103 entries, 0 to 102
    Data columns (total 4 columns):
    PostalCode       103 non-null object
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    address          103 non-null object
    dtypes: object(4)
    memory usage: 4.0+ KB


<H1>Import GeoPy:</H1>


```python
pip install geopy
```

    Requirement already satisfied: geopy in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (1.20.0)
    Requirement already satisfied: geographiclib<2,>=1.49 in /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages (from geopy) (1.50)
    Note: you may need to restart the kernel to use updated packages.



```python
from geopy.geocoders import Nominatim
print('Nominatim imported')
```

    Nominatim imported


<H1>Set connection to OpenStreeMap</H1>


```python
df_geopy['address']=df_geopy['PostalCode'] + ',' + df_geopy['Borough'] + ','+ df_geopy['Neighbourhood']
df_geopy.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B,Scarborough,Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C,Scarborough,Highland Creek,Rouge Hill,Port...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E,Scarborough,Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G,Scarborough,Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H,Scarborough,Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
nom = Nominatim()
n=nom.geocode('M1B, Scarborough, Rouge,Malvern')
n
n.latitude
```

    /home/jupyterlab/conda/envs/python/lib/python3.6/site-packages/ipykernel_launcher.py:1: DeprecationWarning: Using Nominatim with the default "geopy/1.20.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      """Entry point for launching an IPython kernel.





    geopy.location.Location




```python
type(n)
n2=nom.geocode('M1E Scarborough Guildwood,Morningside,West Hill')
print(n2)
```

    None


<H1>Use 'address' to get geocode coordinates:</H1>


```python
df_geopy['Coordinates'] =df_geopy['address'].apply(nom.geocode)
df_geopy.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
      <th>Coordinates</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B,Scarborough,Rouge,Malvern</td>
      <td>(Malvern, Scarborough—Rouge Park, Scarborough,...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C,Scarborough,Highland Creek,Rouge Hill,Port...</td>
      <td>None</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E,Scarborough,Guildwood,Morningside,West Hill</td>
      <td>None</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G,Scarborough,Woburn</td>
      <td>(Woburn, Scarborough—Guildwood, Scarborough, T...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H,Scarborough,Cedarbrae</td>
      <td>None</td>
    </tr>
  </tbody>
</table>
</div>




```python
<H2>COORDINATES</H2>
```


```python
df_geopy.info()
df_geopy.Coordinates[0]
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 103 entries, 0 to 102
    Data columns (total 5 columns):
    PostalCode       103 non-null object
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    address          103 non-null object
    Coordinates      5 non-null object
    dtypes: object(5)
    memory usage: 4.8+ KB





    Location(Malvern, Scarborough—Rouge Park, Scarborough, Toronto, Golden Horseshoe, Ontario, M1B 4Y7, Canada, (43.8091955, -79.2217008, 0.0))




```python
print(df_geopy.Coordinates[1])
```

    None



```python
df_geopy['latitude']=df_geopy['Coordinates'].apply(lambda x: x.latitude if x !=None else None)
df_geopy['longitude']=df_geopy['Coordinates'].apply(lambda x: x.longitude if x !=None else None)
df_geopy.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
      <th>Coordinates</th>
      <th>latitude</th>
      <th>longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B,Scarborough,Rouge,Malvern</td>
      <td>(Malvern, Scarborough—Rouge Park, Scarborough,...</td>
      <td>43.809196</td>
      <td>-79.221701</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C,Scarborough,Highland Creek,Rouge Hill,Port...</td>
      <td>None</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E,Scarborough,Guildwood,Morningside,West Hill</td>
      <td>None</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G,Scarborough,Woburn</td>
      <td>(Woburn, Scarborough—Guildwood, Scarborough, T...</td>
      <td>43.759824</td>
      <td>-79.225291</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H,Scarborough,Cedarbrae</td>
      <td>None</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_geopy.to_csv('geo_loc_py.csv')
```

<TEXT>As just 5 addresses were fruitful, we will go on to use the given geo-location csv.</TEXT>


```python
print('The latitude of', df_geopy.address[0],  'is', df_geopy.latitude[0], 'and its longitude is',df_geopy.longitude[0])
```

    The latitude of M1B,Scarborough,Rouge,Malvern is 43.8091955 and its longitude is -79.2217008


<H1>2. Used the csv file to create the requested dataframe</H1>


```python
# Load the Pandas libraries with alias 'pd' 
import pandas as pd 
# Read data from file 'filename.csv' 
# (in the same directory that your python process is based)
# Control delimiters, rows, column names with read_csv (see later) 
data2 = pd.read_csv("geopy.csv") 
# Preview the first 5 lines of the loaded data 
data2.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B, Scarborough, Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C, Scarborough, Highland Creek,Rouge Hill,Po...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E, Scarborough, Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G, Scarborough, Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H, Scarborough, Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
data3 = pd.read_csv("http://cocl.us/Geospatial_data") 
# Preview the first 5 lines of the loaded data 
data3.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Postal Code</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
  </tbody>
</table>
</div>




```python
data3.rename(columns={'Postal Code': 'PostalCode'}, inplace=True)
data3.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
  </tbody>
</table>
</div>




```python
data1 = pd.merge(data3, data2, how='inner', on=None, left_on=None, right_on=None,
         left_index=False, right_index=False, sort=True,
         suffixes=('_x', '_y'), copy=True, indicator=False,
         validate=None)

data1.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Latitude</th>
      <th>Longitude</th>
      <th>Unnamed: 0</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>43.806686</td>
      <td>-79.194353</td>
      <td>0</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>M1B, Scarborough, Rouge,Malvern</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>43.784535</td>
      <td>-79.160497</td>
      <td>1</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>M1C, Scarborough, Highland Creek,Rouge Hill,Po...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>43.763573</td>
      <td>-79.188711</td>
      <td>2</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>M1E, Scarborough, Guildwood,Morningside,West Hill</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>43.770992</td>
      <td>-79.216917</td>
      <td>3</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>M1G, Scarborough, Woburn</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>43.773136</td>
      <td>-79.239476</td>
      <td>4</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>M1H, Scarborough, Cedarbrae</td>
    </tr>
  </tbody>
</table>
</div>




```python
data1.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 103 entries, 0 to 102
    Data columns (total 7 columns):
    PostalCode       103 non-null object
    Latitude         103 non-null float64
    Longitude        103 non-null float64
    Unnamed: 0       103 non-null int64
    Borough          103 non-null object
    Neighbourhood    103 non-null object
    address          103 non-null object
    dtypes: float64(2), int64(1), object(4)
    memory usage: 6.4+ KB



```python
cols = data1.columns.tolist()
cols
new_column_order = ['PostalCode',
 'Borough',
 'Neighbourhood',
 'Latitude',
 'Longitude']
new_column_order
```




    ['PostalCode', 'Borough', 'Neighbourhood', 'Latitude', 'Longitude']




```python
data1 = data1[new_column_order]
data1.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M1B</td>
      <td>Scarborough</td>
      <td>Rouge,Malvern</td>
      <td>43.806686</td>
      <td>-79.194353</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1C</td>
      <td>Scarborough</td>
      <td>Highland Creek,Rouge Hill,Port Union</td>
      <td>43.784535</td>
      <td>-79.160497</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1E</td>
      <td>Scarborough</td>
      <td>Guildwood,Morningside,West Hill</td>
      <td>43.763573</td>
      <td>-79.188711</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M1G</td>
      <td>Scarborough</td>
      <td>Woburn</td>
      <td>43.770992</td>
      <td>-79.216917</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M1H</td>
      <td>Scarborough</td>
      <td>Cedarbrae</td>
      <td>43.773136</td>
      <td>-79.239476</td>
    </tr>
  </tbody>
</table>
</div>




```python
sorted_df = data1.sort_values([ 'Neighbourhood', 'Latitude'], ascending=[True, True])
sorted_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>58</th>
      <td>M5H</td>
      <td>DowntownToronto</td>
      <td>Adelaide,King,Richmond</td>
      <td>43.650571</td>
      <td>-79.384568</td>
    </tr>
    <tr>
      <th>12</th>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
      <td>43.794200</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <th>14</th>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North,L'Amoreaux East,Milliken,Steel...</td>
      <td>43.815252</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <th>101</th>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens,Beaumond Heights,Humbergate,Jam...</td>
      <td>43.739416</td>
      <td>-79.588437</td>
    </tr>
    <tr>
      <th>89</th>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood,Long Branch</td>
      <td>43.602414</td>
      <td>-79.543484</td>
    </tr>
  </tbody>
</table>
</div>




```python
sorted_df.reset_index(inplace=True)
sorted_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>index</th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>58</td>
      <td>M5H</td>
      <td>DowntownToronto</td>
      <td>Adelaide,King,Richmond</td>
      <td>43.650571</td>
      <td>-79.384568</td>
    </tr>
    <tr>
      <th>1</th>
      <td>12</td>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
      <td>43.794200</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <th>2</th>
      <td>14</td>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North,L'Amoreaux East,Milliken,Steel...</td>
      <td>43.815252</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <th>3</th>
      <td>101</td>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens,Beaumond Heights,Humbergate,Jam...</td>
      <td>43.739416</td>
      <td>-79.588437</td>
    </tr>
    <tr>
      <th>4</th>
      <td>89</td>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood,Long Branch</td>
      <td>43.602414</td>
      <td>-79.543484</td>
    </tr>
  </tbody>
</table>
</div>




```python
sorted_cols =sorted_df.columns.tolist()
sorted_cols
```




    ['index', 'PostalCode', 'Borough', 'Neighbourhood', 'Latitude', 'Longitude']




```python
new_column_order2 = ['PostalCode',
 'Borough',
 'Neighbourhood',
 'Latitude',
 'Longitude']
new_column_order2
```




    ['PostalCode', 'Borough', 'Neighbourhood', 'Latitude', 'Longitude']




```python
sorted_dataframe = sorted_df[new_column_order]
sorted_dataframe.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PostalCode</th>
      <th>Borough</th>
      <th>Neighbourhood</th>
      <th>Latitude</th>
      <th>Longitude</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>M5H</td>
      <td>DowntownToronto</td>
      <td>Adelaide,King,Richmond</td>
      <td>43.650571</td>
      <td>-79.384568</td>
    </tr>
    <tr>
      <th>1</th>
      <td>M1S</td>
      <td>Scarborough</td>
      <td>Agincourt</td>
      <td>43.794200</td>
      <td>-79.262029</td>
    </tr>
    <tr>
      <th>2</th>
      <td>M1V</td>
      <td>Scarborough</td>
      <td>Agincourt North,L'Amoreaux East,Milliken,Steel...</td>
      <td>43.815252</td>
      <td>-79.284577</td>
    </tr>
    <tr>
      <th>3</th>
      <td>M9V</td>
      <td>Etobicoke</td>
      <td>Albion Gardens,Beaumond Heights,Humbergate,Jam...</td>
      <td>43.739416</td>
      <td>-79.588437</td>
    </tr>
    <tr>
      <th>4</th>
      <td>M8W</td>
      <td>Etobicoke</td>
      <td>Alderwood,Long Branch</td>
      <td>43.602414</td>
      <td>-79.543484</td>
    </tr>
  </tbody>
</table>
</div>


