# ATMS523-Project-SF

Title: Time Series and EOF Analysis with Monthly ERA-5 Data for a 30-year Temperature and Precipitation Analysis in the Upper Colorado River Basin (UCRB)

Motivation: The climate in the UCRB now seems to be facing the possibility of aridification. It may one day go from a semi-arid environment to an arid environment. I want to do a basic analysis of the temperature and precipitation data to determine if aridification is influencing the greater UCRB area. 

Scientific question to be answered: Over the last 30 years, how has temperature and precipitation patterns changed the Upper Colorado River Basin (UCRB)? By utilizing ERA-5 data,  can a successful investigation be done on the possibility of aridification in the UCRB?

Project goal: Find any trends, patterns, or possible evidence that the UCRB could be going through the beginning motions of aridification. 

Project finidngs:
The data analysis uncovered climatologically interesting trends and opened up avenues for further analysis. I sought to find any common patterns or trends that point to beginning signs of aridification through seasonal decomposition and EOF analysis. There are many publications and peer-reviewed studies on the aridification of the CRB that indicate somber findings that the CRB is going from a semi-arid to arid environment. I think the patterns and trends found during this analysis also coincide with these research studies. If this were more nuanced and had more variables, multiple analysis approaches, and even different packages involved it could provide better results. However, this is merely a starting point.

Packages used: 
import xarray as xr
import pandas as pd
import geopandas as gpd 
import numpy as np 
import datetime as datetime 
import cartopy.crs as ccrs
import cartopy.feature as cfeature
import matplotlib.pyplot as plt
from pylab import rcParams
from sklearn.linear_model import LinearRegression
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa import api as smt
from statsmodels.tsa.seasonal import seasonal_decompose
from statsmodels.tsa.stattools import adfuller
import dask
from dask.distributed import Client, progress
import geopandas as gpd
import os
import matplotlib.cm as cmap 
from eofs.xarray import Eof
import warnings
warnings.filterwarnings("ignore", category=UserWarning, module="cartopy")

Analysis methods used: 
Data visualization
Basic Decomposition
EOF Analysis
Pearson Correlation

Sources: 
Shapefile: https://www.sciencebase.gov/catalog/item/4f4e4a38e4b07f02db61cebb
Climate data: https://thredds.rda.ucar.edu/thredds/dodsC/aggregations/g/ds633.1/2/TP