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

- **Simple** (one row, one marker)
- **Cluster** (many rows, one marker / geographical proximity)
- **Choropleth** (one row, one marker / marker color gradiet <=> numerical column values)
- **Category** (one row, one marker / marker color <=> distinct column values)
- **Bubble** (one row, one marker / marker size <=> numerical column values)
- **Torque, Torque Cat** (animation over time)
- **Heatmap, Torque Heatmap** (density map)
- **Intensity** (think Simple + Cluster)
- **Density** (hex density grid)

#### Infowindow

Infowindows pop up after clicking on a map marker. Choose what information to display and how to style it. Or disable Infowindows completely.

***Note:If Infowindow button is disabled, your current visualization does not support this feature***

#### CartoCSS

CSS-like stylesheets for changing appearance of map elements. You can choose a wizard and then customize the styles, or write your own from scratch.

***Note: styles in the editor are reset when you change to a different visualization using the wizards***

#### Legends

Some wizard visualizations support legends automatically. If yours doesn't, you can make your own.

## CartoDB.js
