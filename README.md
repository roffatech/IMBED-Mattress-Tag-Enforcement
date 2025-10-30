The purpose of Generate-200-coordinates.py is to generate 200 (or any number you want, you can edit the script) latitude/longitude coordinates within a rectangular region. 

It is not enforced, but if you are using this to generate sample data, you should choose a region that does not include private residences to avoid any problems with privacy issues. 

You can obtain this region any way you like as long as you come up with starting and ending latitude/longitude coordinates that form a rectangular region. 

One relatively easy way to get such a region is to use OpenStreetMap as follows. 

1. Use the Search field to position the map area to a specific location like a city. Enter the city name and click the magnifying glass button. 

2. Position the map so that the area you want to define as a region is present. You can drag and zoom to narrow it down. In a video I made recently, I did this in Bloomington, IN in the U.S. The video is at https://www.youtube.com/watch?v=nQXxFHwcRXo.

3. Once you have located an area, click the Export option on the OpenStreetMap menu bar.

4. Then click the option "Manually select a different area". If you do not choose this option, then the whole region on the screen will be used, it's possible the are will include private residences, which we generally want to avoid.

5. After clicking that option, much of the map area darkens except for an area with 'handles' in the corners. This is your rectangular region. Drag the handles to move the boundaries to your preferred position

6. Once you have your region positioned as you want it, click the blue Export button. This creates an OSM file that will appear in your Downloads. This is basically an XML file. Open the file in another tab. I did this in Windows 11 by viewing my Downloads and clicking the OSM file name. This shoud open in another tab. 

7. About 2-3 lines in, select and copy the line with the <bounds> tag. This should contain minlat, minlon, maxlat, and maxlon values.
   
8. Open the Generate-200-coordinates.py file in your Python environment. I will assume for the sake of keeping this README simple that you have your Python environment setup properly.
   
9. Paste the <bounds> tag you copied from step 7 into the code and replace the minlat, minlon, maxlat, and maxlon values in the code with those in the tag. Be sure to remove anything that would cause a syntax error when running the script.
    
10. You can change other values in the script as you see fit, like the CSV file name or the number of random points generated.
    
11. Once your code is ready, run the Python script and examine your CSV file. You can import these into a table for mapping later. You can also repeat this process for other areas depending on how you want your sample heat map to look. 

12. Generating the heat map itself is beyond the scope of this code, but you can feed this data to OpenStreetMap and other sources, or to an AI engine to get a map with these points in it. Double check the point-plotting to make sure the points are in the areas you expect them to be. 
