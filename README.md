# Data-Representation-and-Querying-Project-2015

# Galway City Car Parking Locations

### Tim Daiber

## Introduction

This project provides the design and documentation for the dataset "Galway City Car Parking Locations" which is available at https://data.gov.ie/dataset/galway-city-car-parking-locations



## Dataset
The dataset "Galway City Car Parking Locations" privides the user with usefull information about the location of parking places in Gawlay. The location is represented in lonatude and latitude also the amount of parking spaces can be gathered from the dataset.
The CSV file contains 14 columns and 29 rows.

Dataset Column breakdown.
 
|Heading | Description  |
|---------|-----------|
| X | Geographic Coverage on the x axis |
| Y | Geographic Coverage on the y axis |
| ObjectID | Revers to the ID of the individual parking space |
| Name |  Name of the Parking Space|
| Type" | Declares the restiriction|
| NO_SPACES | The max amount of cars the carpark can hold|
| Lat | Referes to latitude (Geographic Location Coordinates from north to south position)|
| Long | Referes to longitude (Geographic Location Coordinates from east-west position)|
| EastITM | East-west ITM (Irish Transverse Mercator) is the geographic coordinate system for Ireland|
| NorhtITM | North ITM (Irish Transverse Mercator) is the geographic coordinate system for Ireland|
| EastIG | Easting are geographic Cartesian coordinates for a point|
| NorthIG | Northing are geographic Cartesian coordinates for a point|

####Row example for ID:

- **X**: -9.053499750875776
- **Y**: 53.27308246983011
- **ObjectID**: 1
- **Name**: Market St               
- **Type**: Pay/Surface Carpark
- **NO_SPACES**: 88
- **Lat**: 53.273
- **Long**: -9.054
- **EastITM**: 529691.955
- **NorhtITM**: 725294.803
- **EastIG**:  129726.012
- **NorthIG**: 225265.639

### URL Example One

To get a Parking lot by there ID:
http://galwayparking.com/parking/objectid/[objectid]

Example for ID 1:
http://galwayparking.com/parking/objectid/1

 JSON Response Example:

 ```json
 [
    {
    "X":-9.053499750875776,
    "Y":53.27308246983011,
    "OBJECTID":1,
    "NAME":"Market St",
    "TYPE":"Pay/Surface Carpark",
    "NO_SPACES":88,
    "Lat":53.273,
    "Long":-9.054,
    "EastITM":529691.955,
    "NorthITM":725294.803,
    "EastIG":129726.012,
    "NorthIG":225265.639
  }
  ]
 ```

 XML response example:

```xml
<ROWSET>
<ROW>
<X>-9.053499750875776</X>
<Y>53.273082469830108</Y>
<OBJECTID>1</OBJECTID>
<NAME>Market St</NAME>
<TYPE>Pay/Surface Carpark</TYPE>
<NO_SPACES>88</NO_SPACES>
<Lat>53.273</Lat>
<Long>-9.054</Long>
<EastITM>529691.955</EastITM>
<NorthITM>725294.803</NorthITM>
<EastIG>129726.012</EastIG>
<NorthIG>225265.639</NorthIG>
</ROW>
</ROWSET>
```

#### URL example for Name:

http://galwayparking.com/parking/name/[name]

http://galwayparking.com/parking/name/salthill

JSON response:
(will return an array of all Parking lots with the name salthill)
 
 ```json
[
    {
        "X":-9.07333841029907,
        "Y":53.2596098335674,
        "OBJECTID":13,
        "NAME":"Salthill",
        "TYPE":"Surface Carpark (free parking)",
        "NO_SPACES":,
        "Lat":53.26,
        "Long":-9.074,
        "EastITM":528346.431,
        "NorthITM":723815.637,
        "EastIG":128380.202,
        "NorthIG":223786.148
    },
        {
        "X":-9.076039760436448,
        "Y":53.259010763215024,
        "OBJECTID":14,
        "NAME":"Salthill",
        "TYPE":"Surface Carpark (free parking)",
        "NO_SPACES":,
        "Lat":53.259,
        "Long":-9.077,
        "EastITM":528165.221,
        "NorthITM":723751.7,
        "EastIG":128198.954,
        "NorthIG":223722.195
    },
    {...}
]
 ```
 
 XML example:
 
 ```xml
 <ROWSET>
 <ROW>
<X>-9.073338410299071</X>
<Y>53.259609833567403</Y>
<OBJECTID>13</OBJECTID>
<NAME>Salthill</NAME>
<TYPE>Surface Carpark (free parking)</TYPE>
<NO_SPACES> </NO_SPACES>
<Lat>53.26</Lat>
<Long>-9.074</Long>
<EastITM>528346.431</EastITM>
<NorthITM>723815.637</NorthITM>
<EastIG>128380.202</EastIG>
<NorthIG>223786.148</NorthIG>
</ROW>
<ROW>
<X>-9.076039760436448</X>
<Y>53.259010763215024</Y>
<OBJECTID>14</OBJECTID>
<NAME>Salthill</NAME>
<TYPE>Surface Carpark (free parking)</TYPE>
<NO_SPACES> </NO_SPACES>
<Lat>53.259</Lat>
<Long>-9.077</Long>
<EastITM>528165.221</EastITM>
<NorthITM>723751.7</NorthITM>
<EastIG>128198.954</EastIG>
<NorthIG>223722.195</NorthIG>
</ROW>
<ROW>
...
</ROWSET>
```

### URL / Web address makeup

http://galwayparking.com/parking

> HTTP:HyperText Transfer Protocol

> www.galwayparking.com: Domain name

> .com: extension (i.e.: .ie ireland)

> /parking: PATH to specific page within a site

### Filters

Example of using filters to filter out unwanted data:

http://galwayparking.com/parking/?[filter]=[parameter]

Using filters to just show multistory carparks:

http://galwayparking.com/parking/?type=Multistorey&Carpark

### Get method

Example for get method:

Get Parking Space with ID 4

http://galwayparking.com/parking/?OBJECTID=4

### Put method

Using put method to update existing values

http://galwayparking.com/parking/update?objectid=[id]&values=[value]

Example of updating the number of spaces in a carpark from 0 to 102

http://galwayparking.com/parking/update?objectid=5&field=no_spaces&value=102


### Delete method

This will probably not be used since Parking spaces lots get taken down but I will include it anyway.

Deletes parking spaces with name salthill

http://galwayparking.com/parking/name/salthill/delete

DELETE parking/name/galwayparking.html / HTTP/1.1

host: www.galwayparking.com

name="salthill"

...

###Post 

If Galway would ever get more carparks what is very likely in a growing city the post command could look like

http://galwayparking.com/parking/name/new

POST parking/name/galwayparking.html HTTP/1.1

HOST: www.galwayparing.com

Connection: Keep-Alive

Content-type: text/html

x=-9.053499751&y=53.27308247&objectid=19&name=St.Cresent&Type=Multistorey&NO_SPACES=300&Lat=53.273&Long...

#### Terminology

API - Application Programming Interface

REST API - REpresentational state Transfer

JSON - JavaScript Object Notation

Graph API:
Example: graph.galwayparking.com/parking/no_spaces

Maps API:
Example: map.galwayparking.com/parking

#### Resources

https://www.youtube.com/watch?v=7YcW25PHnAA

https://www.youtube.com/watch?v=576WwU7xlWU

