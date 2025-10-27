# ERA5 Pacific SST & TCRW EOF Analysis (1979–2024)
## By: Nathan Makowski, ATMS 523, Fall 2025 

## Overview
This project analyzes monthly mean Sea Surface Temperature (SST) and Total Column Rain Water / Water Vapor (TCRW) over the Pacific Basin (65°S–65°N, 120°E–60°W) using ERA5 data. The analysis includes:

- Subsetting and masking ocean points.
- Detrending and deseasonalizing SST and TCRW anomalies.
- Standardizing SST anomalies.
- Performing Empirical Orthogonal Function (EOF) analysis.
- Reconstructing SST using leading EOFs.
- Correlating SST EOF1 (PC1) with TCRW anomalies.

## Dataset
- **Source:** ERA5 monthly mean data © ECMWF, distributed via Copernicus Climate Data Store.
- **Shared by:** Megan Walker (via Dropbox, classroom peer).
- **Time period:** 1979–2024
- **Spatial domain:** Pacific Basin, 65°S–65°N, 120°E–60°W
- **Resolution:** ~1° x 1° (after coarsening)
- **Variables:** SST, TCRW
- **File format:** NetCDF (`.nc`)

## Files Produced
- `era5_pacific_sst_tcrw_1deg_1979_2024.nc`: deseasonalized and detrended SST & TCRW anomalies
- EOF correlation maps and reconstruction correlation plots (matplotlib figures)

## Python Packages Required
```python
import numpy as np
import xarray as xr
import matplotlib.pyplot as plt
import cartopy.crs as ccrs
import cartopy.feature as cfeature
from eofs.xarray import Eof

## License 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

- **Data License:**

The ERA5 data used in this project are © European Centre for Medium-Range Weather Forecasts (ECMWF) and distributed via the Copernicus Climate Data Store (CDS) under the Copernicus Licence Agreement.
Use of these data must comply with the Copernicus Data Policy and is independent of the MIT License applied to this project’s source code.