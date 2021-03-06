## Sample geopackages

The sample unprojected (geographic, MOON, IAU sphere) geopackages are supposed to work with [Mappy](https://github.com/europlanet-gmap/mappy), i.e. 
geologic units are defined as points, and polygons are generated dynamically as needed, based on contat intersections.

 ## Qgis project CRS
 
 The geographic projection is already included in e.g. QGIS 3.16. Other projection could be set as needed (procedure to be documented) with GDAL/OGR
 
 ```
 GCS_Moon_2000
WKT
GEOGCRS["GCS_Moon_2000",
    DATUM["D_Moon_2000",
        ELLIPSOID["Moon_2000_IAU_IAG",1737400,0,
            LENGTHUNIT["metre",1]]],
    PRIMEM["Reference_Meridian",0,
        ANGLEUNIT["degree",0.0174532925199433]],
    CS[ellipsoidal,2],
        AXIS["geodetic latitude (Lat)",north,
            ORDER[1],
            ANGLEUNIT["degree",0.0174532925199433]],
        AXIS["geodetic longitude (Lon)",east,
            ORDER[2],
            ANGLEUNIT["degree",0.0174532925199433]],
    USAGE[
        SCOPE["unknown"],
        AREA["World"],
        BBOX[-90,-180,90,180]],
    ID["ESRI",104903]]
Proj4
+proj=longlat +R=1737400 +no_defs
Extent
-180.00, -90.00, 180.00, 90.00
```

## GMAP geopackages

The template (provided here for the Moon, using an set of empty geopackages with geographic coordinates) includes

* Units (point)
* Contacts (line)
* Surface features (polygon)
* Linear features (line)

The layers used actively by Mappy are _Units_ and _Contacts_. Additional vector layers are possible, see also [GMAP wiki](https://wiki.europlanet-gmap.eu/bin/view/Main/Documentation/Vector%20mapping%20fields/)
