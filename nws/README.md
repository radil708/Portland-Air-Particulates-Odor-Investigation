
# NWS data

Weather observations for PWM (Portland International Jetport)

## Iowa State data source

The GUI is easy to use and constructs a URL that can be put into a script. I put it in the Makefile.

* https://mesonet.agron.iastate.edu/request/download.phtml?network=ME_ASOS
  * Query for all data, 1 Jan 2020 to 28 Aug 2021...
  * https://mesonet.agron.iastate.edu/cgi-bin/request/asos.py?station=PWM&data=all&year1=2020&month1=1&day1=1&year2=2021&month2=8&day2=28&tz=Etc%2FUTC&format=onlycomma&latlon=yes&elev=no&missing=M&trace=T&direct=no&report_type=1&report_type=2

## NCDC data source

This is a NOAA data source -- I used it to download 2696191.csv.

* https://www.ncdc.noaa.gov/homr/#ncdcstnid=30125525&tab=MSHR
  * Portland Jetport -- 1820-01-01 to Present
  * PORTLAND FT WILLIAMS, ME 1944-01-01 to 1945-07-31
* https://www.ncdc.noaa.gov/homr/#ncdcstnid=20009702&tab=MSHR -- NCDC site with other links
* NCEI for historical data
  * https://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:USW00014764/detail
  * CSV downloaded from: https://www.ncdc.noaa.gov/cdo-web/confirmation
* data dictionary
  * WSF2 - Fastest 2-minute wind speed
  * WSF5 - Fastest 5-second wind speed
  * SNOW - Snowfall
  * WT03 - Thunder
  * PRCP - Precipitation
  * WT05 - Hail (may include small hail)
  * WT06 - Glaze or rime
  * WT08 - Smoke or haze
  * SNWD - Snow depth
  * WDF2 - Direction of fastest 2-minute wind
  * AWND - Average wind speed
  * WDF5 - Direction of fastest 5-second wind
  * PGTM - Peak gust time
  * WT01 - Fog, ice fog, or freezing fog (may include heavy fog)
  * TMAX - Maximum temperature
  * WT02 - Heavy fog or heaving freezing fog (not always distinguished from fog)
  * TAVG - Average Temperature.
  * TMIN - Minimum temperature
