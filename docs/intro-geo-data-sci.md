## Introduction to Geospacial Data Science

<img src="https://upload.wikimedia.org/wikipedia/commons/5/55/Carbon_cycle-cute_diagram.jpeg" width=840/>
Image credit: Wikimedia Commons

***


## Introduction

[**Earth science or geoscience**](https://en.wikipedia.org/wiki/Earth_science) includes all fields of natural science related to the planet Earth. This is a branch of science dealing with the physical, chemical, and biological complex constitutions and synergistic linkages. Earth science encompasses four main branches of study the [biosphere](https://en.wikipedia.org/wiki/Biosphere), the [hydrosphere](https://en.wikipedia.org/wiki/Hydrosphere), the  [atmosphere](https://en.wikipedia.org/wiki/Atmosphere), and the [lithosphere](https://en.wikipedia.org/wiki/Lithosphere), each of which is further broken down into more specialized fields.

[Python](https://www.python.org) is a widely used, open-source programming language. In Earth science, scientific programming languages like Python, help you speed up and automate lengthy tasks like selecting and downloading large datasets or performing repetitive calculations that you might otherwise have to do manually.

Depending on the type of scientific application sensor or measuring device, geoscience associated data is stored in many [formats and data types](https://gisgeography.com/gis-formats/). We need to be aware of this, so we can plan how to read data into our analysis environment.

## Basic Python Libraries

There is a set of basic general Python libraries that allows us to perform data analysis and data visualization. They involve a set of data structures, available mathematical operations, defined statistical analysis functions and a collection of different functions to visualize data properties.

* [**numpy**](https://numpy.org). _NumPy_ is the fundamental library for scientific computing in Python. It provides a multidimensional array object, various derived objects (such as masked arrays and matrices), and an assortment of routines for fast operations on arrays, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, basic statistical operations, random simulation and more.
* [**matplotlib**](https://matplotlib.org). _Matplotlib_ is the main plotting library for Python. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits. A more popular and user friendly visualization library derived from Matplotlib is [_Seaborn_](https://seaborn.pydata.org).
* [**pandas**](https://pandas.pydata.org/). _Pandas_ is a Python software library for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series. It is free software released under the three-clause BSD license.
* [**scipy**](https://scipy.org). SciPy is a free and open-source Python library used for scientific computing and technical computing. It includes modules for optimization, linear algebra, integration, interpolation, special functions, FFT, signal and image processing, ODE solvers and other tasks common in science and engineering.

## Python Libraries for Geospatial Data

There is a collection of available Python Libraries to work with spatially distribuited data. We mention a list of the most relevant ones.

### Essential General Python Libraries

* [**dask**](https://www.dask.org). _Dask_ is a flexible library for parallel computing in Python.
* [**kerchunk**](https://fsspec.github.io/kerchunk/). Kerchunk is a library that provides a unified way to represent a variety of chunked, compressed data formats (e.g. NetCDF/HDF5, GRIB2, TIFF, …), allowing efficient access to the data from traditional file systems or cloud object storage.
*  [**numba**](https://numba.pydata.org). _Numba_ is an open source [JIT compiler](https://en.wikipedia.org/wiki/Just-in-time_compilation) that translates a subset of Python and NumPy code into fast machine code.
* [**pystac**](https://pystac.readthedocs.io/en/stable/). _PySTAC_ is a library for working with [SpatioTemporal Asset Catalogs (_STAC_)](https://stacspec.org/en).
* [**stackstac**](https://pypi.org/project/stackstac/). Load a _STAC_ collection into xarray with dask.
* [**xarray**](https://docs.xarray.dev/en/stable/index.html). _Xarray_ is an open source project and Python package that introduces labels in the form of dimensions, coordinates, and attributes on top of raw NumPy-like arrays, which allows for more intuitive, more concise, and less error-prone user experience.
* [**xarray-spatial**](https://xarray-spatial.org). _Xarray-Spatial_ implements common raster analysis functions using Numba and provides an easy-to-install, easy-to-extend codebase for raster analysis.
* [**zarr**](https://zarr.readthedocs.io/en/stable/). _Zarr_ is a format for the storage of chunked, compressed, N-dimensional arrays.
### Essential Geospatial Python libraries For Raster Data

* [**GDAL**](https://gdal.org/). _GDAL_ is a translator library for [_raster_](https://en.wikipedia.org/wiki/Raster_graphics) and [_vector_](https://en.wikipedia.org/wiki/Vector_graphics) geospatial data formats that is released under an MIT style Open Source License by the [_Open Source Geospatial Foundation_](https://www.osgeo.org/).
* [**RasterFrames**](https://rasterframes.io/). _RasterFrames_ brings together Earth-observation (EO) data access, cloud computing, and DataFrame-based data science. The recent explosion of EO data from public and private satellite operators presents both a huge opportunity and a huge challenge to the data analysis community.
* [**rasterio**](https://rasterio.readthedocs.io/en/latest/index.html). _Rasterio_ allows access to geospatial [_raster_](https://en.wikipedia.org/wiki/Raster_graphics) data.
* [**rasterstats**](https://pythonhosted.org/rasterstats/index.html). _Rasterstats_ is a Python module for summarizing geospatial raster datasets based on vector geometries. It includes functions for zonal statistics and interpolated point queries. The command-line interface allows for easy interoperability with other [_GeoJSON_](https://geojson.org/) tools.
* [**RSGISLib**](http://rsgislib.org/about.html).The _Remote Sensing and Geographical Information Systems software Library (RSGISLib)_, contains a number of algorithms for processing and analysing remote sensing data that are the product of research carried out by the authors and their collaborators. 

### Essential Geospatial Python libraries For Vector Data

* [**fiona**](https://fiona.readthedocs.io/en/latest/). _Fiona_ focuses on reading and writing data in standard Python IO style and relies upon familiar Python types and protocols such as files, dictionaries, mappings, and iterators. Fiona can read and write real-world data using multi-layered GIS formats and zipped virtual file systems and integrates readily with other Python GIS packages such as [pyproj](https://pypi.org/project/pyproj/), [Rtree](https://pypi.org/project/Rtree/), and [Shapely](https://shapely.readthedocs.io/en/stable/).

* [**GDAL/OGR**](https://gdal.org/programs/index.html#vector-programs). Several software programs use the GDAL/OGR libraries to allow them to read and write multiple GIS formats.
* [**geomesa**](https://www.geomesa.org/). GeoMesa is an open source suite of tools that enables large-scale geospatial querying and analytics on distributed computing systems. GeoMesa provides spatio-temporal indexing on top of the Accumulo, HBase, Google Bigtable and Cassandra databases for massive storage of point, line, and polygon data. GeoMesa also provides near real time stream processing of spatio-temporal data by layering spatial semantics on top of Apache Kafka. 
* [**geopandas**](https://geopandas.org/en/stable/). _GeoPandas_ is an open source Python library for working geospatial data. GeoPandas extends the datatypes used by [pandas](https://pandas.pydata.org/) to allow spatial operations on geometric types. Geometric operations are performed by [shapely](https://shapely.readthedocs.io/en/stable/). GeoPandas further depends on [fiona](https://fiona.readthedocs.io/en/latest/) for file access and [matplotlib](https://matplotlib.org/) for data visualization.
* [**pyproj**](https://pypi.org/project/pyproj/). Python interface to [_PROJ_](https://proj.org/) (cartographic projections and coordinate transformations library).
* [**shapely**](https://shapely.readthedocs.io/en/stable/). _Shapely_ is a BSD-license Python package for manipulation and analysis of planar geometric objects. 

### Essential Geospatial Python libraries For Point Clouds

* [**PDAL**](https://pdal.io/en/latest/index.html). _PDAL_ is a C++ library for translating and manipulating [point cloud data](https://en.wikipedia.org/wiki/Point_cloud). It is very much like the [GDAL](https://gdal.org/) library which handles raster and vector data. 
* [**laspy**](https://laspy.readthedocs.io/en/latest/index.html). [LAS](https://www.asprs.org/divisions-committees/lidar-division/laser-las-file-format-exchange-activities) (and its compressed counterpart LAZ), is a popular format for lidar point cloud and full waveform, _laspy_ reads and writes these formats and provides a Python API via Numpy Arrays.
* [**numpy**](https://numpy.org). _NumPy_ is the fundamental library for scientific computing in Python. When combined with a reader/writer library like _LasPy_, we can store point cloud data in a NumPy array, as well as filter/process the data. NumPy is also good for general use across the geospatial domain.

### Essential Geospatial Python libraries For Visualization

* [**cartopy**](https://scitools.org.uk/cartopy/docs/latest/index.html). _Cartopy_ is a Python package designed for geospatial data processing in order to produce maps and other geospatial data analyses. Cartopy makes use of the powerful [PROJ]((https://proj.org/)), [NumPy](https://numpy.org) and [Shapely](https://shapely.readthedocs.io/en/stable/) libraries and includes a programmatic interface built on top of [Matplotlib](https://matplotlib.org) for the creation of publication quality maps.
* [**geoplotlib**](https://github.com/andrea-cuttone/geoplotlib). _geoplotlib_ is a Python toolbox for visualizing geographical data and making maps.
* [**ipyleaflet**](https://ipyleaflet.readthedocs.io/en/latest/). _ipyleaflet_ creates interactive maps in a Jupyter Notebook. 
* [**Folium**](https://python-visualization.github.io/folium/). An alternative to _Ipyleaflet_, _Folium_ is also a bridge to `leaflet.js`. The difference between the two is that _Folium_ is built toward static visualizations, whereas _Ipyleaflet_ builds interactive widgets. A useful feature of _Folium_ is that it provides easy functionality to export an interactive map to HTML, making it a useful tool in web development.
* [**TorchGeo**](https://github.com/microsoft/torchgeo). [TorchGeo](https://torchgeo.readthedocs.io/en/stable/) is a PyTorch domain library, similar to [torchvision](https://pytorch.org/vision/stable/index.html), providing datasets, samplers, transforms, and pre-trained models specific to geospatial data.


***

## References

* [Earth Lab](https://www.earthdatascience.org). Resources developed by [Earth Lab at University of Colorado](https://earthlab.colorado.edu), Boulder. The website contains, course lessons and blog posts related to earth data science.
* [Project Pythia](https://projectpythia.org). An education and training hub for the geoscientific Python community.
* Ryan Abernathey. [An Introduction to Earth and Environmental Data Science](https://earth-env-data-science.github.io/intro.html).
* Michael Dorman. [Introduction to Spatial Data Programming with Python](https://geobgu.xyz/py/index.html).  Department of Geography and Environmental Development, Ben-Gurion University of the Negev.
*  Dani Arribas-Bel [A course on Geographic Data Science](https://darribas.org/gds_course/content/home.html). University of Liverpool.
* Henrikki Tenkanen, Vuokko Heikinheimo & David Whipp. [Introduction to Python for Geographic Data Analysis](https://pythongis.org/index.html). 
*  Sergio J. Rey, Dani Arribas-Bel, Levi J. Wolf. [Geographic Data Science with Python](https://geographicdata.science/book/intro.html).
* Michael Szell. [Geospatial Data Science](https://github.com/mszell/geospatialdatascience). University of Copenhagen.
*  [The Ultimate List of GIS Formats and Geospatial File Extensions](https://gisgeography.com/gis-formats/). GISGeography.

***
Created: 08/18/2022;
Updated: 03/14/2023

Carlos Lizárraga.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/CC_BY-NC-SA.svg/800px-CC_BY-NC-SA.svg.png?20181117113353" width="150" height="50"/> [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)


[<img src="https://datascience.arizona.edu/sites/default/files/Data%20Science%20Institute_Webheader%20%281%29.svg" width="256">](https://datascience.arizona.edu)


