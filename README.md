# Air Quality WebGIS — Switzerland

An interactive Vue and OpenLayers site for exploring Swiss air-quality patterns, land cover, and population exposure.

[Open the live WebGIS](https://yiyilv.github.io/air_pollution_web/#/)

![PM2.5 and population bivariate map for Switzerland](src/assets/bivariate_PM2P5.png)

## Project question

How do air-pollution concentrations, land cover, and population exposure vary across Switzerland, and how can these patterns be explored on a map?

## Workflow

The project presents annual NO₂, PM₂.₅, and PM₁₀ analysis for 2013–2022, an ESA CCI land-cover classification, and population-exposure maps using 2020 WorldPop data. The site includes project workflow and results pages, annual concentration tables, trend charts, exposure summaries, and a WebGIS with OpenStreetMap or satellite basemaps and pollutant/land-cover layer controls.

The project pages identify CAMS reanalysis, ESA CCI land cover, WorldPop, and FAO administrative boundaries as data sources. The published workflow describes GIS processing with QGIS/GRASS and serves map layers through GeoServer WMS; the front end uses Vue, OpenLayers, and Tailwind CSS.

## My contribution

The project's Developers page attributes air-quality data analysis and workflow content to Yiyi Cen. The public repository and site identify this as a student team project.

## Run locally

```sh
npm install
npm run serve
```

Create a production build with `npm run build`.

## Deployment and service dependency

The live site is hosted on GitHub Pages. The interactive data layers depend on the project GeoServer WMS endpoint configured in `src/components/MapContainer.vue`; that source currently uses an HTTP URL. Confirm HTTPS availability for that service before claiming every data overlay works in modern browsers, since HTTP layers can be blocked on an HTTPS page.

The project is an educational geospatial application. Its front end and screenshots do not include a complete, independently reproducible GIS preprocessing pipeline or a versioned data package.

## Data sources

- [CAMS European air-quality reanalysis](https://ads.atmosphere.copernicus.eu/datasets/cams-europe-air-quality-reanalyses)
- [ESA CCI land cover](https://cds.climate.copernicus.eu/datasets/satellite-land-cover)
- [WorldPop population data](https://hub.worldpop.org/geodata/listing?id=29)
- [FAO Global Administrative Unit Layers](https://data.apps.fao.org/catalog/dataset/b0634117-37c0-4125-ad87-89cb9aec4eea)
