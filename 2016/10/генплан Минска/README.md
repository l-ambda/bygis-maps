Генплан Минска

Скачан 2016-10-30, адрес http://minsk.gov.by/share/2010/04/08/data/20161012.gp.jpg

Основные положения генплана:
http://minsk.gov.by/share/2010/04/08/data/20161012.generalplan.main.pdf

Регламенты генплана:
http://minsk.gov.by/share/2010/04/08/data/20161012.generalplan.rules.pdf


Конвертация в mbtiles:

wget http://minsk.gov.by/share/2010/04/08/data/20161012.gp.jpg
привязать в qgis с помощью плагина georeferencer
gdalwarp 20161012.gp_modified.tif -t_srs EPSG:3857 -co "ZOOM_LEVEL_STRATEGY=UPPER" -co "ZLEVEL=9" -co "TILE_FORMAT=PNG8" -co "TYPE=baselayer" -tr 9.554628535647032 9.554628535647032 -of mbtiles 20161012.gp.mbtiles
gdaladdo -oo "ZLEVEL=9" -oo "TILE_FORMAT=PNG8" 20161012.gp.mbtiles 2 4 8