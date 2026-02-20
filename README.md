# Traffic Safety in Seattle (2022)

## AI Disclosure
No AI used in this assignment.

This project is an interactive web map of 2022 traffic safety conditions in Seattle. It integrates collision records with traffic flow counts to support exploratory analysis of where severe crashes and high-risk road segments are located.

## Data Sources

1. **Seattle Department of Transportation (SDOT) collision data (2022)**  
   
2. **SDOT traffic flow count data (2022)**  
   
All data are from 2022: SDOT collision records and traffic flow counts.

Both local GeoJSON datasets are stored in Washington State Plane (EPSG:2926) and are reprojected in the web app to WGS84 for web mapping display.

## Main Functions of the Map

- Displays three interactive layers:
  - Traffic volume lines (AWDT/ADT)
  - Computed traffic risk index lines
  - Collision point symbols
- Supports layer toggles for volume, risk, and collisions.
- Provides click popups for collision details (severity, date, type, weather) and risk-segment details.
- Computes a **risk index** for each traffic segment: `crashes / (AWDT + 1)`.
- Ranks and lists top high-risk segments and supports click-to-zoom from the list.
- Updates a side-panel summary for the current map extent:
  - Visible collision count
  - Severity chart 
- Includes a reset button to return to the default map view.

## Thematic Map Type and Why

This project uses a **proportional symbol map** as its primary thematic representation (collision points).

Why proportional symbols were chosen:

- Collision events are point-based observations, so point symbols preserve event locations directly.
- Symbol size and color encode severity magnitude in an intuitive way.
- A choropleth map would require aggregation into polygons (such as tracts or neighborhoods), which can hide street-level patterns.



## Map URL (GitHub Pages)

- [https://martinnnYuan.github.io/geog458_lab06/map.html](https://martinnnYuan.github.io/geog458_lab06/map.html)

