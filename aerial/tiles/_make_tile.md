`gdal_translate -of GTiff -a_ullr 116.335963 39.954054 116.443325 39.865712 -a_srs EPSG:4269 1966.jpg 1966.tif`

`gdal_translate -co COMPRESS=JPEG -co JPEG_QUALITY=20 -co PHOTOMETRIC=YCBCR 1959_modified.tif 1959_compressed.tif`

`gdalwarp -of GTiff -co COMPRESS=JPEG -co PHOTOMETRIC=YCBCR -t_srs EPSG:3857 1966.tif 1966_warp.tif`

/check gdal ver/
/pip3 install gdal==ver/
/which python3 to get python dir/
/which gdal2tiles.py to locate gdal2tiles.py/
/edit headline to make gdal2tiles.py run python3/

`gdal2tiles.py -z 12-17 _fullsize/1966_warp.tif tiles/1966/`


  W:116.335963e,  S:39.865712° N
  E: 116.443325e,  N:39.954054°N