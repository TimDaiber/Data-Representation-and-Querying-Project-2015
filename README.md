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

###Row example:

- **X**: -9.053499750875776
- **Y**: 53.27308246983011
- **ObjectID**: 1
- **Name**:            Market St               
- **Type**: Pay/Surface Carpark
- **NO_SPACES**: 88
- **Lat**: 53.273
- **Long**: -9.054
- **EastITM**: 529691.955
- **NorhtITM**: 725294.803
- **EastIG**:  129726.012
- **NorthIG**: 225265.639


## JSON Example

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

##XML example
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

[Apps4gaps](http://apps4gaps.ie/) have asked you design a simple API to any of their datasets.


> From Joshua Bloch's "How to Design a Good API and Why it Matters"

> *Characteristics of a Good API*
> - *Easy to learn*
> - *Easy to use, even without documentation*
> - *Hard to misuse*
> - *Easy to read and maintain code that uses it*
> - *Sufficiently powerful to satisfy requirements*
> - *Easy to extend*
> - *Appropriate to audience*



