# stinky

## Northeastern University student projects

### Smell reports

Summer 2021 term - links to Jupyter notebooks. (Links at the top of these notebooks will open them automatically in Colab).

1. Files for updating data (these notebooks clean and merge raw data, as needed)
* [stinky_dataset.ipynb](https://github.com/ds5110/stinky/blob/master/stinky_dataset.ipynb) -- Use to update df_stinky, table that combines data from SmellMyCity and SeeClickFix
* [oil_vessel_dataset.ipynb](https://github.com/ds5110/stinky/blob/master/oil_vessel_dataset.ipynb) -- Use to update df_vessels, table that contains merged, annual data tracking oil vessel passages through Portland

2. Files with students' analyses
* [text_analysis.ipynb](https://github.com/ds5110/stinky/blob/master/text_analysis.ipynb) -- Analyzes the text of smell descriptions and builds visualizations based on these analyses. Includes attempts at building a classifier, which would allow us to tag each row by smell type. Methods and results of each attempt are described in order to help build a better classifier in the future.
  * [huggingface_results.ipynb](https://github.com/ds5110/stinky/blob/master/huggingface_results.ipynb) -- Includes results from one of the classifier attempts in text_analysis.ipynb. The model takes ~30 minutes to run; results were downloaded and loaded into huggingface_results.ipynb for easy reference. See "Approach 4: Use Huggingface" in text_analysis.ipynb.
* [distributions_allvars_analysis.ipynb](https://github.com/ds5110/stinky/blob/master/distributions_allvars_analysis.ipynb) -- Includes visualizations regarding the pattern of complaints on a monthly basis and relates it to different factors such as arrival of vessels, type of oil carried by these vessels, average temperature, average wind speed and also distributes the complaints according to the city of Portland and South Portland. Convenience functions are made to make the analysis user friendly as the distributions can be changed for different months and year.
* [stinky_maps.ipynb](https://github.com/ds5110/stinky/blob/master/stinky_maps.ipynb) -- Merge the df_Stinky data with weather data and visualise the geographical data on the basis of temperature, wind direction and season. Plotting pods and terminals as well for better understanding. The data is visualised region wise (Portland and South Portland) and weather data is considered from the nearest pod only.

### Environmental sensors

* All raw pod measurements are uploaded to the "stinky/weather_data_raw" directory in this repo. Those files are in the form of .csv. To update this repo simply replace the pod file. Thre replacement file needs to keep the original file naming scheme.

1. Files for personal download (this notebook will autmatically download the weather group's data sets - just run to download. These files do not need to moved to the repo - they can used for personal analyses). These files are also present in the directiory weather_data/intermediary_files/
* [weather_datasets.ipynb](https://github.com/ds5110/stinky/blob/master/weather_datasets.ipynb)

2. This notebook contains the visualizations and analyses performed by the weather team - weather feature plots, logistic modeling, etc. Text descriptions are included.
* [Weather_Team_Analysis_Notebook.ipynb]

### Data files - description of data folders and individual file names

1. Data folders
* data: contains raw data (csv files) of smell data (from SmellMyCity and SeeClickFix), and tidied csv files merging raw smell data and oil vessels data
* vessels_data_raw: contains raw data (csv files) for data tracking oil vessel passages through Portland
* weather_data_raw: contains raw data (csv files) for weather data

2. Data files
* df_stinky.csv: this file is the tidied and merged file containing odor complaints from both SmellMyCity(smc.csv) and SeeCLickFix(scf.csv). This file is used for all other analytical notebooks and further analysis.
* df_vessels.csv: this file is the tidied and merged file containing oil vessels data for year 2020 (2020 SMRO VESSEL ARRIVALS.csv) and year 2021 (2021 SMRO VESSEL ARRIVALS.csv). This file is used for all other analytical notebooks and further analysis.
* huggingface_results.csv: results from a model run in text_analysis.ipynb. The model takes ~30 minutes to run; results were downloaded and loaded into huggingface_results.ipynb for easy reference. To update with new data in df_stinky and download: see instructions in text_analysis.ipynb.
* scf.csv: it is the original file with odor complaints from SmellMyCity
* smc.csv: it is the original file with odor complaints from SeeClickFix
* 2020 SMRO VESSEL ARRIVALS.csv: it is the original file containing all of oil vessels data for year 2020 
* 2021 SMRO VESSEL ARRIVALS.csv: it is the original file containing all of oil vessels data for year 2021

## Project Idea: This Stinks

Problem: Residents of Portland and South Portland in Maine have been reporting disruptive smells in the air 
on certain days of the year. 
South Portland has over 25,500 residents, and is the host of oil, gasoline, and asphalt tanks. 
These tanks do not have emissions controls and the emissions, in the form of odors, 
are reported in both South Portland and Portland. 
Many of the emissions are odorless and toxic, and may or may not correlate with odor complaints. 
It's been unclear what the source of the smells might be and difficult to understand the extent of the 
issue on both sides of the Fore River, which separates Portland and South Portland.

The City of South Portland relies on [Smell My City](https://smellmycity.org/) for odor complaints, 
while Portland relies on [See Click Fix](https://seeclickfix.com/portland_2).
The Department of Environmental Protection has 
[9 VOC Canister Monitors](https://www.maine.gov/dep/air/monitoring/spo-sampling-results.html)
(volatile organic compounds) in Portland and South Portland. 
The tanks are considered [minor sources of air emissions](https://www.maine.gov/dep/air/permits/minor.html),
and regulated accordingly.

### Project goals.

* Coordinate the various data sources
  * Smell My City odor complaints (South Portland)
  * See Click Fix odor complaints (Portland)
  * DEP VOC sampling data
  * Civilian grab canister results
  * Tom Mikulka monitoring data (for comparison only)
  * Weather patterns
  * Tank fills and transfers (dependent on access to data)
  * Individual tank inventory and temperature status
* Clean the data and make it easily accessible for the general public
* Create some simple visualizations
* Add additional data from ME DEP (e.g., wind speed, direction, temperature, etc)
Initial mapping will use compiled data, but the intent is to harvest data in real time to account 
for established correlations, additional sampling, and continued monitoring. 
Per [LD163](http://www.mainelegislature.org/legis/bills/getPDF.asp?paper=HP0119&item=2&snum=130), 
additional sampling will include: 
* Fenceline monitoring (continuous)
* Self reported emissions testing on heated tanks (2x yearly)

### Project partners

* The Greater Portland Council of Governments (GPCOG)
* The Sierra Club
* Roux Institute

## data

* Excel spreadsheet -- for City of Portland, Maine
  * [SeeClickFix](https://seeclickfix.com/portland_2) app for Portland residents
  * residents add odor reports with the app
  * these reports are collected by the city and sent (to us) monthly in an excel file
* https://smellmycity.org/data
  * This site has directions for accessing South Portland odor complaints
  * Enter ZIP codes of interest (South Portland have several ZIP codes) 
  * This produces a spreadsheet for download
* https://rainwise.net/weather/SMRO3
  * This site has DEP weather reports. 
  * The top drop-down menu has reports of interest to the project. 
  * There are many stations, only a portion of them are online
  * SMRO 3-7 (the units that are online) -- note the location at the bottom of the page. 
  * These were installed sometime in 2020 (that's when ME DEP started monitoring South Portland in particular)
  * To download spreadsheets, hit the button at the top of the bar that is a downward arrow.
* Oil terminals -- all of this data is in paper form
  * When barges come into the Portland terminal to deliver or pick up oil, they have to give DEP notice
  * There are written notifications from boats to ME DEP -- these are faxed paper copies
  * We hope to be be getting this data...

## key people

* Maria Guerra (Environmental Health Fellow, [Resilience Corps](https://www.gpcog.org/472/Resilience-Corps) at GPCOG)
* Andrew Butcher (Director of Innovation & Resilience, [GPCOG](https://www.gpcog.org))
* Luke Truman (Sierra Club's Maine Chapter)
  * Luke has experience in data mapping, and working on projects with college students.
  * He has been invested in this problem of Portland/South Portland air quality for some time.
