# inventory-dashboard

As described by [The Global Historical Climatology Network](https://www.ncdc.noaa.gov/data-access/land-based-station-data/land-based-datasets/global-historical-climatology-network-ghcn), the GHCN is an integrated database of climate summaries 
from land surface stations across the 
globe that have been subjected to a common suite of quality assurance reviews. 
The data are obtained from more than 20 sources. Some data are more than 175 years old while 
others are less than an hour old.

# Description of Project
Provide a visualization dashboard for the station data included in the GHCN Archive.
The purpose was to evaluate the spatial distribution and temporal evolution of the stations in the archive.
The analysis conditions on the type of measurements available and the continents of the stations.  For stations in 
North America, the analysis also considers the type of station.

# Methods
1.  Python was used to download the source files and setup the local directory structure:
    [inventory.ipynb](https://nbviewer.jupyter.org/github/douglasdrake/inventory-dashboard/blob/master/inventory.ipynb).
2.  Pandas was used to clean the data, merge data frames and produce summary statistics for the station data.
3.  CartoPy, Geoplot, matplotlib, and seaborn were used to produce plots: 
    [density.ipynb](https://nbviewer.jupyter.org/github/douglasdrake/inventory-dashboard/blob/master/density.ipynb) and
    [northamerica.ipynb](https://nbviewer.jupyter.org/github/douglasdrake/inventory-dashboard/blob/master/northamerica.ipynb).
    The density plots use a function I had written before that outputs a GeoJSON.  To use Geoplot, the GeoJSON is converted to a GeoPandas
    GeoDataFrame of Shapely objects.
4.  An analysis of the distribution of nearest neighbor distances between stations was performed:
    [nearest-neighbor-distance.ipynb](https://nbviewer.jupyter.org/github/douglasdrake/inventory-dashboard/blob/master/nearest-neighbor-distance.ipynb)
4.  HTML.  The layout of each page of the dashboard is done with [Bootstrap](https://getbootstrap.com/).  Navigational bars, drop-down menus, and tables all use Bootstrap components.
5.  CSS.  Images and component characteristics are modified with a CSS style sheet.
6.  The dashboard uses responsive web design to adjust the layout and image sizes based on the user's device.

The [dashboard](https://douglasdrake.github.io/inventory-dashboard/).

## Citation:
Menne, M.J., I. Durre, R.S. Vose, B.E. Gleason, and T.G. Houston, 2012:  *An overview 
of the Global Historical Climatology Network-Daily Database*.  Journal of Atmospheric 
and Oceanic Technology, 29, 897-910, doi:10.1175/JTECH-D-11-00103.1.

Menne, M.J., I. Durre, B. Korzeniewski, S. McNeal, K. Thomas, X. Yin, S. Anthony, R. Ray, 
R.S. Vose, B.E.Gleason, and T.G. Houston, 2012: *Global Historical Climatology Network - 
Daily (GHCN-Daily)*, Version 3.27.
