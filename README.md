## ArcMap workshop for PLHRT 4400


# Getting started

We will be using a network drive that has been set up with data files and map documents.  Each student should have read and write access to this folder.

1. Open the Windows File Explorer (yellow folder icon at bottom of screen)
2. Right-click "This PC" > Map Network Drive...
3. Drive = `L:`
4. Folder = `\\files.cornell.edu\fs\dept\ua_cpo\sharedgis\student_share`
5. Press "Finish" and wait for it to connect

Once it connects, the folder should open automatically.  If it fails, try again...

Each student should have an .mxd file named "Restoration Ecology Project_" followed by their NetID.


# Exploring the map

Double-click the .mxd file with your NedID to open your map.

We'll spend some time exploring the map, turning on different layers, changing the symbology, etc.


# Adding another shapefile

To add a polygon shapefile of plant communities:

1. File menu > Add Data > Add Data...
2. In the ArcMap file dialog, browse to Home > GIS Sourcefiles
3. Select and add `NA carbon project.shp`

rename to "Plant Communities"
attribute table, indentify tool
symbology by category
transparency

# Adding another basemap

The map document already includes NYS imagery from various years.  We can add the latest 2018 imagery via the NYS Web Map Service.

1. Add Data
2. Look in: "GIS Servers"
3. Add ArcGIS Server
4. Select "Use GIS services"
5. Server URL = http://www.orthos.dhses.ny.gov/arcgis/services
6. Double-click `arcgis on www.orthos.dhses.ny.gov`
7. Add the 2018 layer

Wait for the layer to be added to the map.  Depending on where it appears in the table of contents, you may need to move it up or down, or turn off other layers for it to be visible.

For more details about the NYS Orthoimagery, see https://gis.ny.gov/gateway/mg/

```



go outside, collect GPS waypoints
have a backup .gpx file just in case
convert to shapefile from gpx
edit -- add dbh, species columns

layouts
scale bar, north arrow, legend
export map image - formats, dpi
```




