## Cloud Native Data in Geosciences.

<img src="https://opensource.com/sites/default/files/lead-images/rh_003601_05_mech_osyearbook2016_cloud_cc.png" width=480>

(Image credit: Opensource.com)

There is a shift is happening in the way we use Earth Science data to do new research. Cloud data storage technologies have advanced at a fast pace that we now can find and explore massive amounts of data online via the web browser. At the same time we can find online platforms with specialized software and hardware that offer general data science and machine learning tools to explore these online datasets.

With these advances it is easier to foster collaborations, promote data-driven discovery, scientific innovation, transparency and reproducibility.

## Open Architectures

The new approach to data sharing, focused on object storage rather than file downloads. This cloud platform approach is scalable and instead of moving data to processing systems near users as is the tradition, brings processing, computing, analytics and visualization to data – so called data proximate workbench capabilities, sometimes also referred to as server-side processing.

<img src="https://miro.medium.com/max/1400/1*FkR2h8f_Lut00Uo_Pxogvg.png" width=480>

(Open Architecture for scalable cloud-based data analytics. From Abernathey, Ryan (2020): Data Access Modes in Science.)

***

## Cloud Data Types

We will be reviewing the next set of data types
* [GeoJSON](https://geojson.org/)
* [Cloud Optimized GeoTiff (COG)](https://www.cogeo.org/)
* [Cloud Optimized Point Clouds (COPC)](https://copc.io/)

***

### GeoJSON

[GeoJSON](https://en.wikipedia.org/wiki/GeoJSON) is a format that supports encoding a wide variety of gegraphic data structures using JavaScript Object Notation (JSON) [[RFC7159](https://datatracker.ietf.org/doc/html/rfc7159)].  A
GeoJSON object may represent a region of space (a Geometry), a
spatially bounded entity (a Feature), or a list of Features (a
FeatureCollection).

It has the following format:
```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [125.6, 10.1]
  },
  "properties": {
    "name": "Dinagat Islands"
  }
}

```

Where the "type" can be any of the following:

| Type | Geometry |
| :--: | :--:     |
|Point   |  ![Point](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/SFA_Point.svg/51px-SFA_Point.svg.png)|
| LineString   |  ![Linestring](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b9/SFA_LineString.svg/51px-SFA_LineString.svg.png)|
|Polygon   |   ![Polygon](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/SFA_Polygon.svg/51px-SFA_Polygon.svg.png) |
|MultiPoint|  ![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d6/SFA_MultiPoint.svg/51px-SFA_MultiPoint.svg.png)  |
| MultiLineString  |    ![MultiLineString](https://upload.wikimedia.org/wikipedia/commons/thumb/8/86/SFA_MultiLineString.svg/51px-SFA_MultiLineString.svg.png)|
|MultiPolygon   |  ![MultiPolygon](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3b/SFA_MultiPolygon_with_hole.svg/51px-SFA_MultiPolygon_with_hole.svg.png)
| GeometryCollection | ![GeometryCollection](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/SFA_GeometryCollection.svg/51px-SFA_GeometryCollection.svg.png) |

Read more about the [GeoJSON format](https://datatracker.ietf.org/doc/html/rfc7946).

### COG

The [TIFF file format (Tagged Image File Format)](https://en.wikipedia.org/wiki/TIFF) is a very old format, dating back to 1992, which is great for high-resolution, verbatim [raster images](https://en.wikipedia.org/wiki/Raster_graphics). It’s still used a bit in high-end photography, but has really grown a second life in cartography: a variation called [GeoTIFF](https://en.wikipedia.org/wiki/GeoTIFF) is used to share satellite images and other satellite data.

The GeoTIFF file format has long been thought of as only suitable for raw data: if you wanted to display it on a map, you’d convert it into tiles. If you wanted a static image, you’d render it into a PNG or JPEG. But [Cloud-Optimized GeoTIFF](https://en.wikipedia.org/wiki/GeoTIFF#Cloud_Optimised_GeoTIFF) means that GeoTIFFs can be a bit more accessible than they used to be.

A [Cloud Optimized GeoTIFF (COG)](https://www.cogeo.org/) is a regular [GeoTIFF file](https://en.wikipedia.org/wiki/GeoTIFF), aimed at being hosted on a HTTP file server, with an internal organization that enables more efficient workflows on the cloud. It does this by leveraging the ability of clients issuing ​HTTP GET range requests to ask for just the parts of a file they need.

Built to support efficient tile-by-tile access to large collections of geospatial imagery, the COG has provided an excellent template for the development of other cloud-optimized data formats (e.g. [Zarr](https://zarr.readthedocs.io/en/stable/index.html)).

Like many open source projects, the development and production of COGs has lead to innovation in other areas as well. One example of such innovation is the development of the [SpatioTemporal Asset Catalog (STAC)](https://stacspec.org/en).

The SpatioTemporal Asset Catalog (STAC) specification provides a common language to describe a range of geospatial information, so it can more easily be indexed and discovered. A ‘spatiotemporal asset' is any file that represents information about the earth captured in a certain space and time.

COGs and STAC provide the building blocks for a flexible and accessible system for geospatial data analysis (geospatial imagery). STAC provides a system for describing large collections of geospatial data stored in cloud object store and COG provide efficient access to pieces of those collections without the need to download the data first.

#### Python libraries needed to work with COG files

The following libraries are needed:
* [rasterio](https://rasterio.readthedocs.io/en/latest/index.html). Geographic information systems use GeoTIFF and other formats to organize and store gridded raster datasets such as satellite imagery and terrain models. Rasterio reads and writes these formats and provides a Python API based on Numpy N-dimensional arrays and GeoJSON.
* [pyproj](https://pyproj4.github.io/pyproj/stable/). Python interface to [PROJ](https://proj.org) (cartographic projections and coordinate transformations library).
* [sat-search](https://github.com/sat-utils/sat-search). Sat-search is a Python 3 library and a command line tool for discovering and downloading publicly available satellite imagery using STAC compliant API.

### COPC






### Spatio Temporal Asset Catalogs (STAC)


[STAC](https://stacspec.org/en) provides a common language to describe a range of spatiotemporal information, so that it can be easily indexed and discovered.

The goal is for all providers of spatiotemporal assets (Imagery, SAR, Point Clouds, Data Cubes, Full Motion Video, etc) to expose their data as SpatioTemporal Asset Catalogs (STAC), so that new code doesn't need to be written whenever a new data set or API is released.

A STAC item is the foundational building block of STAC. It is [GeoJSON](https://en.wikipedia.org/wiki/GeoJSON) supplemented with additional metadata that enables clients to traverse through catalogs.

The [STAC Index](https://stacindex.org) stores STAC Catalogs, Collections, APIs, Software and Tools.

To access the STAC Index catalogs, the [`pystac-client`](https://github.com/stac-utils/pystac-client) libary needs to be installed.





## References

* [Introduction to Cloud Native & Analysis Ready Data Formats](https://tyson-swetnam.github.io/agic-2022/). Tyson L. Swetnam, Carlos Lizárraga.
* [Cloud Optimized GeoTIFF ](https://www.cogeo.org). An imagery format for cloud-native geospatial processing. COGEO.org.
* Gentemann, C. L., Holdgraf, C., Abernathey, R., Crichton, D., Colliander, J., Kearns, E. J., et al. (2021). [Science storms the cloud. AGU Advances, 2, e2020AV000354](https://agupubs.onlinelibrary.wiley.com/doi/epdf/10.1029/2020AV000354)
* Ryan P. Abernathey _et al._ (2021) [Cloud-Native Repositories for Big Scientific Data. Computing in Science and Engineering. IEEE Computer Society](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9354557)
* Abernathey, R. (2020). [Closed Platfoms vs. Open Architectures for Cloud-Native Earth System Analytics](https://medium.com/pangeo/closed-platforms-vs-open-architectures-for-cloud-native-earth-system-analytics-1ad88708ebb6). Pangeo, Medium.
* Holmes, C. (2021). [STAC Specification 1.0.0 Released](https://medium.com/radiant-earth-insights/stac-specification-1-0-0-released-c59e8c848077). Radiant Earth Insights, Medium.
* Holmes, C. (2018).[Cloud Native Geoprocessing](https://medium.com/planet-stories/tagged/cloud-native-geospatial). Planet Stories, Medium.

***
Created: 08/18/2022;
Updated: 08/27/2022

Carlos Lizárraga.
UA Data Science Institute.
