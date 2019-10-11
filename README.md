## ArcMap workshop for PLHRT 4400


# Map the network drive

We will be using a network drive that has been set up with data files and map documents.  Each student should have read and write access to this folder.

1. Open the Windows File Explorer (yellow folder icon at bottom of screen)
2. Right-click "This PC" > Map Network Drive...
3. Drive = `L:`
4. Folder = `\\files.cornell.edu\fs\dept\ua_cpo\sharedgis\student_share`
5. Press "Finish" and wait for it to connect

Once it connects, the folder should open automatically.  If it fails, ignore the error and try again.  If you follow these instructions exactly, it usually connects after 2 tries, despite the error messages.  Sometimes it helps to reboot the computer first.

Each student should have an .mxd file named "Restoration Ecology Project_" followed by their NetID.


# Explore the map

Double-click the .mxd file with your NetID to open your map.

We'll spend some time exploring the map, turning on different layers, changing the symbology, etc.


# Add a shapefile

To add a polygon shapefile of plant communities:

1. File menu > Add Data > Add Data...
2. In the ArcMap file dialog, browse to Home > GIS Sourcefiles
3. Select and add `NA carbon project.shp`
4. Right-click the "NA carbon project" layer name > Properties
5. Go to "General" tab, rename as "Plant Communities"

We'll explore this layer via the "Identify" tool and attribute table, then change the symbology by categories, adjust transparency, add labels, etc.


# Adding a basemap

The map document already includes NYS imagery from various years.  We can add the latest 2018 imagery via the NYS Web Map Service.

1. Add Data
2. Look in: "GIS Servers"
3. Add ArcGIS Server
4. Select "Use GIS services"
5. Server URL = http://www.orthos.dhses.ny.gov/arcgis/services
6. Double-click `arcgis on www.orthos.dhses.ny.gov`
7. Add the 2018 layer

Wait for the layer to be added to the map.  Depending on where it appears in the table of contents, you may need to move it up or down, or turn off other layers for it to be visible.

8. Rename the layer to "2018 Ortho Imagery" (using the same method we used for the shapefile)

For more details about the NYS Orthoimagery, see https://gis.ny.gov/gateway/mg/


# Collect GPS data

We'll go outside and collect GPS waypoints for some individual trees, noting the size and species on paper, something like this:

| NAME | DBH | SPECIES |
| ---- | --- | ------- |
| 1    | 13  | Fraxinus americana |
| 2    |  7  | Fraxinus americana |
| 3    | 20  | Fraxinus americana |
| 4    | 12  | Fraxinus americana |

Copy the .gpx file from the GPS unit to your personal folder under `Student_Share/Student Projects`.  (If we run into any trouble getting the data from the GPS units, copy the backup GPX file `Student_Share/GIS Sourcefiles/gps_backup/gps_points.gpx` to your folder.)

We may need to use Garmin's BaseCamp to transfer the data:

1. Install Garmin BaseCamp: https://www8.garmin.com/support/download_details.jsp?id=4435
2. Connect the GPS to the computer via a USB cable
3. Turn on the GPS unit
4. Open BaseCamp. The GPS unit should show up under "devices"
5. Click on the GPS unit name to view its internal storage
6. Highlight your points
7. Click file -> export -> export selection
8. Save points to your project folder

ArcMap can read .gpx files, but it will be more reliable to convert it to a shapefile first.

1. Open ArcToolbox (under the Geoprocessing menu)
2. Conversion Tools > From GPS > GPX To Features
3. For the "input GPX file", browse to select the .gpx file in your personal folder.
4. For the "output feature class", browse to your personal folder and save there with filename `gps_points_shapefile.shp`

The new shapefile will be automatically added to the map.  To add the DBH and SPECIES information to the table:

1. Open the attribute table.
2. Via the menu under the first icon, Add Field: Name = DBH, Type = Double
3. Add Field: Name = SPECIES, Type = Text
4. Right-click a blank space in the toolbar area and toggle on the "Editor" toolbar
5. Under the Editor memu, "Start Editing" and select the gps_points_shapefile layer.  Ignore any warnings.
6. Double-cilck a cell to enter the value.  Fill in all the DBH and SPECIES cells.
7. Under the Editor memu, "Stop Editing" and save your edits.

Try changing the symbology of your GPS points to use graduated symbols based on the DBH values.


# Page Layout

Thus far, we've been viewing an infinite view of the world with no edges to the map.  To print or save a map image, we'll create a page layout.

1. "View" menu > Layout View

The scale bar, north arrow, and legend have already been added (via the "Insert" menu).

2. Adjust the left edge of the map so that it does not cover the legend.
3. Select the legend element, then right-click > Properties to customize.
4. Fix the "CBGardens_primary_RGB" which is supposed to be a logo.  Right-click > properties > update the simple path to point to the logo in the "GIS Sourcefiles" folder.

When you are ready to export the map image:

5. "File" menu > Export Map...

Note the various file types (Adobe Illustrator, PDF, JPEG, etc.)  Depending on your map and export type, you may want to adjust the export resolution (dpi).


# Saving your project

Save your project as an ArcMap 10.4 document, so that it can be checked/graded:

1. "File menu" > Save a Copy...
2. Save as type = ArcMap 10.4 Document
3. You can use the same filename you started with (otherwise it will add a "1" to the filename)
