Схемы строительства сетей и коммуникаций


Скачано 2016-10-30 с http://minsk.gov.by/share/2010/04/08/data/20100419.schema.electrician.pdf

обработка:
pdftoppm -r 600 20100419.schema.electrician.pdf -png > 20100419.schema.electrician.png
optipng 20100419.schema.electrician.png
привязка в QGIS Georeferencer
gdalwarp 20100419.schema.electrician_modified.tif -t_srs EPSG:3857 -co "ZOOM_LEVEL_STRATEGY=UPPER" -co "ZLEVEL=9" -co "TILE_FORMAT=PNG" -tr 19.109257071294063 19.109257071294063 -of mbtiles 20100419.schema.electrician.mbtiles