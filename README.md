# Map Time: CartoDB

## Schedule

**4 - 4:50pm**: Tutorial, CartoDB Editor and CartoDB.js

**4:50 - 5pm**: Break

**5 - 5:45pm**: Guided co-working

**5:45 - 6pm**: Lightning show and tell

## Tutorial data set
- [NYPD Motor Vehicle Collisions](https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions/h9gi-nx95) (NYC OpenData)
- Filter by ZIP code for 10003
- Export as CSV

## Import data into CartoDB
1. "New Dataset" button
2. Upload your CSV file
3. Check that data types are correct

## CartoDB Editor

#### SQL

CartoDB uses [PostgresSQL](http://www.postgresql.org/docs/9.4/interactive/index.html) + [PostGIS](http://postgis.net/)

Example query to get only collision data in which at least one cyclist was injured:
````sql
SELECT * FROM nypd_motor_vehicle_collisions WHERE number_of_cyclist_injured > 0
````

#### Wizards

Visualization wizards allow you to quickly create engaging maps with any kind of data.

- **Simple**: one marker = one data point
- **Cluster**: one marker = many data points (based on geographical proximity)
- **Choropleth**: one marker = one data point (color gradient based on numerical column values)
- **Category**: one marker = one data point (color groups based on distinct column values)
- **Bubble**: one marker = one data point (marker size based on numerical column values)
- **Torque, Torque Cat**:  animation over time
- **Heatmap**: density map (optionally animated using Torque)
- **Intensity**: think **Simple** + **Cluster**
- **Density**: hexagonal density grid

#### Infowindows

Infowindows pop up after clicking on a map marker. Choose what information to display and how to style it. Or disable infowindows completely.

***Note: not all visualizations support infowindows***

#### CartoCSS

CSS-like stylesheets for changing appearance of map elements. You can choose a wizard and then customize the styles, or write your own from scratch.

***Note: the CartoCSS in the editor is reset when you change visualizations using the wizards***

#### Legends

Some visualizations automatically support legends. If not, you can make your own.

## CartoDB.js

Clone this repo and modify `example.html` to customize your infowindows and get a feel for how the JavaScript framework is implemented.

Easy way to develop locally is to run a SimpleHTTPServer in your working directory (from the command line):

`python -m SimpleHTTPServer`

## Resources
- [CartoDB tutorials](http://docs.cartodb.com/tutorials.html)
- [CartoDB.js From the Ground Up](http://academy.cartodb.com/courses/03-cartodbjs-ground-up.html)
- [CartoDB examples](https://github.com/CartoDB/cartodb.js/tree/develop/examples) (GitHub)
- [CartoDB basemaps](https://cartodb.com/basemaps/)
- [Stamen maps](http://maps.stamen.com/)
- [CartoCSS docs](https://github.com/mapbox/carto/blob/master/docs/latest.md)
