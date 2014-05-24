helpful-bits-and-pieces
=======================

### Coordinates Transformation (cgsr1993 to wgs84) 
1. Download [proj446_win32_bin.zip](http://download.osgeo.org/proj/proj446_win32_bin.zip)
2. Unzip and move folder `c:\proj\*.*`
3. Open `cmd' 
4. Execute `set PATH=%PATH%;C:\PROJ\BIN` and `set PROJ_LIB=C:\PROJ\NAD`
5. Create file `points.txt` in which each line there is a coordinate e.g. `409927.8709	684225.1047`
6. Execute the command: cs2cs +proj=tmerc +lon_0=33 +k_0=0.99995 +x_0=200000 +y_0=-3500000 +ellps=WGS84 +towgs84=0,0,0 +units=m +no_defs +to +init=epsg:4326 points.txt>pointsout.txt
7. Check the results in file `pointsout.txt`


