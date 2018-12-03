 # Opening & manipulating Geotif files
 ## Using Python
 - You need GDAL package; a nice way to install it is Conda, which can be installed like next:
      - Download the **bash installer** from [Miniconda](https://conda.io/miniconda.html).    
      - Run the installer using (can change depending on the downloaded installed) 
      ```bash
      bash Miniconda3-latest-Linux-x86_64.sh
      ```

  - Install the package in python console: `conda install gdal`
  - Then to use the package in the following way:
  ```python
  from osgeo import gdal
  ds = gdal.Open('input.tif', gdal.GA_ReadOnly)
  rb = ds.GetRasterBand(1)
  img_array = rb.ReadAsArray()
```
and continue from there.

## Using R
- Refer to this [resource](https://www.earthdatascience.org/courses/earth-analytics/lidar-raster-data-r/introduction-to-spatial-metadata-r/)

## Resources
- [Conda installation](https://conda.io/docs/user-guide/install/linux.html#)
- [Open Geotiff in Python](https://stackoverflow.com/questions/41996079/how-do-i-open-geotiff-images-with-gdal-in-python)
