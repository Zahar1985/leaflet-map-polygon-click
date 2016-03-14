# leaflet-map-polygon-click
Leaflet thematic polygon (choropleth) map, with clickable pop-up windows

## Demo
- http://jackdougherty.github.io/leaflet-map-polygon-click/index.html

## Create your own

See chapter tutorials in http://DataVizForAll.org

###General overview of steps below
- Join a GeoJSON polygon map with spreadsheet data
- Modify color ranges and info box display as needed
- Upload all files to a forked or new GitHub repository, create GitHub pages branch for live web host

###Detailed steps:

- Start with GeoJSON polygon map with no numerical data, such as: ct-towns-simple.geojson
- Import polygon map into http://MapShaper.org. Simplify to reduce size as needed.
- Export as CSV to create spreadsheet of polygon names. In this example, column header is "town"
- Open CSV with any spreadsheet tool. Insert columns of data into the CSV sheet. Use VLOOKUP function if needed.
- Save CSV with new name: ct-towns.csv
- Import ct-towns.csv as second layer into MapShaper.org.
- Use the drop-down to select the polygon map (ct-towns-simple.geojson) as the active, displayed layer.
- Click the Console and enter command to join the CSV table to the GeoJSON polygon
  ```
  -join ct-towns.csv keys=town,town
  ```
- Export the newly joined map with a new filename in GeoJSON format (with this suffix): ct-towns-density.geojson)
- Fork this GitHub repository, or create your own, with these files (or equivalent):
  - index.html
  - script.js
  - style.css
  - ct-towns-density.geojson  (the data file)

- in index.html, fix any reference to the data file
- in script.js, adjust references, range, and colors as noted in code comments
