# NDVI-and-maxConnectedArea

version https://git-lfs.github.com/spec/v1
oid sha256:d086c63599dee3f079cb6a0eac329fa66e1399d3ba6e7fdc2a8cf69438438a70
size 141

This will calculates the NDVI values on each pixel on 4-channel Geotiff satellite image and identify the maximum vegetation area

Python version 3.6.6
Used Rasterio python package and opencv for 4-connected components

Geotiff file channel information
  - Channel 1: Blue
  - Channel 2: Green
  - Channel 3: Red
  - Channel 4: Near infrared (NIR)

Since this image is stored in 16-bit format you will need some preview tool that supports this format(Ex: QGIS)

Calculate NDVI Index:
  NDVI = (NIR - Red) / (NIR + Red)

Normalized Difference Vegetation Index (NDVI) quantifies vegetation by measuring the difference between near-infrared (which vegetation strongly reflects) and red light (which vegetation absorbs). NDVI always ranges from -1 to +1.

Based on the threshold value of NDVI, finally we identified the biggest vegetation found region using 4-connected component method.
