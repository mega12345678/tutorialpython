# PYTHON BASIC

```
# BUKA CITRA

# Import the Python 3 print function

from __future__ import print_function

# Import the "gdal" submodule from within the "osgeo" module

from osgeo import gdal 

# Open a GDAL dataset

dataset = gdal.Open('../../example/LE70220491999322EDC01_stack.gtif', gdal.GA_ReadOnly)

print(dataset)

# TENTANG BAND

# How many bands does this image have?

num_bands = dataset.RasterCount
print('Number of bands in image: {n}\n'.format(n=num_bands))

# How many rows and columns?

rows = dataset.RasterYSize
cols = dataset.RasterXSize
print('Image size is: {r} rows x {c} columns\n'.format(r=rows, c=cols)) 

# What driver was used to open the raster?

driver = dataset.GetDriver()
print('Raster driver: {d}\n'.format(d=driver.ShortName))

# PROYEKSI

# What is the raster's projection?

proj = dataset.GetProjection()
print('Image projection:')
print(proj + '\n')  

# http://ceholden.github.io/open-geo-tutorial/python/chapter_1_GDALDataset.html 

```
