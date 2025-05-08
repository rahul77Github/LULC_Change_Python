# 🛰️ Land Use Change Analysis (2017–2024)

This project presents a geospatial analysis of land use and land cover (LULC) changes between the years 2017 and 2024. It uses classified raster datasets and Python-based spatial analysis tools to quantify, compare, and visualize changes across key land categories. The analysis is intended for academic and research purposes, such as environmental assessment, urban expansion monitoring, and sustainable land planning.

# 📚 Objective

To assess spatial and quantitative changes in land cover classes over a seven-year period using remote sensing data and automated GIS workflows. The project automates the calculation of area statistics, identifies net changes, and visualizes trends in a clear, reproducible format.

# 📁 Project Structure

    Automation.ipynb       # Main Jupyter notebook with code for processing and visualization
    data/
        lulc_2017.tif      # Classified raster for 2017
        lulc_2024.tif      # Classified raster for 2024
    output/
    lulc_change_plot.png   # Final bar plot with table inset
    README.md              # This file

# 🧰 Tools & Libraries 
    pandas  matplotlib  geopandas  rasterio  IPython.display  folium  numpy  shapeply

    ## Recommended to install in conda virtual environment

# 🗺️ Raster Dataset Information 
### The project uses multiple classified raster .tif files downloaded from Esri LivingAtlas based on remote sensing data, generated using supervised classification or land cover mapping algorithms.

#### Dataset Properties:

| Property           | Description                                              |
|-------------------|----------------------------------------------------------|
| **Format**         | GeoTIFF (`.tif`)                                         |
| **CRS**            | EPSG:4326 (WGS84) or source native CRS                   |
| **Pixel Type**     | `uint8` (1 band per file)                                |
| **Spatial Resolution** | Typically 10 meters                                 |
| **Classification** | Integer DN values representing land cover                |
| **File Examples**  | `45Q_20170101-20180101.tif`, `45Q_20230101-20240101.tif` |


    
# 🧪 Key Features

    > Reads classified raster datasets for two time periods (2017, 2024).

    > Calculates per-class land cover area (in km²) using raster cell resolution.

    > Computes net change in land cover classes between years.

    > Generates a horizontal bar plot grouped by land cover type:
        Green: 2017
        Blue: 2024
        Red: Net Change

    > Includes a summary table of values directly in the visualization.

    > Handles inconsistencies (e.g., duplicate labels or capitalization) during processing.   

#  🗂️ Land Cover Categories derived from Esri LivingAtlas LULC classification  
   | DN | Class Name         | Description |
   | -- | ------------------ | ------------ | 
   | 1  | Water              |  Areas where water was predominantly present throughout the year; may not cover areas with sporadic or ephemeral water; contains little to no sparse vegetation, no rock outcrop nor built up features like docks; examples: rivers, ponds, lakes, oceans, flooded salt plains. |
   | 2  | Trees              |  Any significant clustering of tall (~15 feet or higher) dense vegetation, typically with a closed or dense canopy; examples: wooded vegetation,  clusters of dense tall vegetation within savannas, plantations, swamp or mangroves (dense/tall vegetation with ephemeral water or canopy too thick to detect water underneath). |
   | 4  | Flooded Vegetation |  Areas of any type of vegetation with obvious intermixing of water throughout a majority of the year; seasonally flooded area that is a mix of grass/shrub/trees/bare ground; examples: flooded mangroves, emergent vegetation, rice paddies and other heavily irrigated and inundated agriculture. |
   | 5  | Crops              |  Human planted/plotted cereals, grasses, and crops not at tree height; examples: corn, wheat, soy, fallow plots of structured land. |
   | 7  | Built Area         |  Human made structures; major road and rail networks; large homogenous impervious surfaces including parking structures, office buildings and residential housing; examples: houses, dense villages / towns / cities, paved roads, asphalt. |
   | 8  | Bare ground        |  Areas of rock or soil with very sparse to no vegetation for the entire year; large areas of sand and deserts with no to little vegetation; examples: exposed rock or soil, desert and sand dunes, dry salt flats/pans, dried lake beds, mines. |
   | 9  | Snow/Ice           |  Large homogenous areas of permanent snow or ice, typically only in mountain areas or highest latitudes; examples: glaciers, permanent snowpack, snow fields. |
   | 10 | Clouds             |  No land cover information due to persistent cloud cover. |
   | 11 | Rangeland          |  Open areas covered in homogenous grasses with little to no taller vegetation; wild cereals and grasses with no obvious human plotting (i.e., not a plotted field); examples: natural meadows and fields with sparse to no tree cover, open savanna with few to no trees, parks/golf courses/lawns, pastures. Mix of small clusters of plants or single plants dispersed on a landscape that shows exposed soil or rock; scrub-filled clearings within dense forests that are clearly not taller than trees; examples: moderate to sparse cover of bushes, shrubs and tufts of grass, savannas with very sparse grasses or other plants. |


