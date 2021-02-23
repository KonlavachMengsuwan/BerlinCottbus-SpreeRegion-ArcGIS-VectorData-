# BerlinCottbus-SpreeRegion-ArcGIS-VectorData-
Vector Data Ecosystem Analysis with ArcGIS on Berlin-Cottbus Spree region.

title: "Ecosystem Analysis Vector Data Berlin-Cottbus Spree region"
author: "Konlavach"
date: "2/23/2021"
output: html_document

## The spatial extend of the case study region is defined by four counties and one city:
### 1)	Spree-Neiße
### 2)	Oberspreewald-Lausitz
### 3)	Dahme-Spreewald
### 4)	Oder-Spree
### 5)	Cottbus

## Data source:
### 1)	European Union
### 2)	German Federal Institutions
### 3)	State of Brandenburg
### 4)	OpenStreetMap
### 5)	GoogleEarth, GoogleMap

## Project objectives:
### 1) Calculate area of counties
### 2) Calculate area of water protection
### 3) Count number of groundwater measurement station
### 4) Area of forest within a distance of 500 m to water bodies (lakes, rivers)
### 5) Georeference and Google basemap

## Step 1: Download Shapefile 
### Source: 

```
Data source: German Federal Agency for Cartography and Geodes public data for Germany (GeoDataCentre)
Administrative borders: VG250 Germany
Land use model: DLM250
```

## Step 2: Add Shapefile

### Add shapefile 
```
Layer -> Add Data -> Select "German county polygons: vg250_kr.shp"
```

### Add shapefile to legend
```
Legend -> Properties
```
![](AddShapefile.png)<!-- -->

## Step 3: Select relevant county polygons

```
- Open attribute table
- Choose counties: SpreeNeiße, OberspreewaldLausitz, DahmeSpreewald, OderSpree, Cottbus
- Brandenbur counties regional key = 12xxx
- Select
```
![](SelectCottbus.png)<!-- -->

## Step 4: Copy selected features
```
ArcToolBox -> Data Management -> Features -> Copy Feature
```

## Step 5: Update visualization
```
Properties -> Symbology -> Standard symbols -> Categories -> unique values
```
![](Symbology.png)<!-- -->

## Step 6: Dissolve all counties 
```
Geoprocessing -> Dissolve
```
![](Dissolve.png)<!-- -->


