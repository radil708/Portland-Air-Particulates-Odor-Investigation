# Questions for July 21 call with Prof Bogden and Maria Guerra from GPCOG

## About smellmycity data
* Oil data: any update on whether we will have access to the paper data from oil barges (tracking their arrival/departure from the port)?
* Besides the oil barges, are there other possible sources of a petroleum-type smell in this area?
* Can you think of other data that could be useful to identify causes of the odor (e.g. sewage or trash locations/issues)? I found [this for South Portland](https://www.southportland.org/departments/water-resource-protection/about-us/treatment-systems/pump-station-o-m/) - any other resources like this that you can think of?
* Are there questions about this data that you'd like answers to?

Answers:
* Focus on oil as odor source? Yes - that’s the smell residents are reporting, not sewage and trash.
* Full data time range? Maria will try to get data from 2019 but more likely from beginning of 2021.
* Smell value: It’s subjective, the opinion of the resident submitting the complaint. Maria does not think it is very useful, especially since it’s only in 1 dataset (smellmycity). Follow up with Professor later - could use onehot encoding, etc. Also later - look into visualizing smell value on map.
* Oil locations: check [DEP website](https://www.maine.gov/dep/air/monitoring/spo-voc-monitor.html). In the news recently: Citgo, Gulf, Global, Sprague.
* Paper data from oil barges: possibility of getting data in a spreadsheet; Maria will update us ASAP.


## About SCF Odor Report (xlsx file in github)
* Does this come from the SeeClickFix app? Is the data different from the smellmycity data?
* Is it possible to download data directly from the app?
* If not, does the xlsx file include all available data? Date range in file is 7/1/2020 - 6/2/2021.

Answers:
* SCF vs. smellmycity: two different platforms for recording odor complaints. SCF: used by residents of Portland. Smellmycity: used by residents of S Portland.
* SCF data is sent by the city of Portland to Maria, as a spreadsheet. No API or way to get data directly. The city will continue to send updated data to Maria and/or us.

## About environmental data
* Since this data is more general, it would be helpful to get insights from GPCOG and Sierra Club that would help us focus.
  * Are there specific questions about the weather reports that you'd like answers to?
  * Is there any other environmental data that you'd like us to look at?

Answers:
* What to focus on in weather reports: wind direction, wind speed, temperature, raining (y/n) —> anything that would make a smell more potent
* PODs: Maria will send info.
* Alternative weather data: weather reports from airports - good proxy.
* Weather sampling at each location is very localized (within 1 mile radius). We can get exact location (lat/long, address) - Maria will send.
* Wind direction units: degrees, increasing clockwise.
* Aim to include 1 year of data at least.

## About project goals / deliverables wish-list from the GPCOG and Sierra Club: What are the questions that you'd like us to answer? Here are a few guesses - could you help us refine these?
* Cause of the odor (e.g. oil barges, sewage issue)
* Geographical concentration of the odor

Answers:
1. Tidy the datasets
   1. Smell data: bring together the two datasets (SCF and smellmycity). Try to do this in a way that can be easily updated after our project ends.
   1. Environmental data: combine data (currently must be downloaded separately)
2. Leave tools (for tidying data, for running analyses/visualizations) that can be updated after our project ends by non-technical users.

## Github organization
* Keep everything on master branch. Don't use separate branches.
* Use Github like Dropbox/Google drive: upload files when they're ready to share. Ok to upload updated versions but document each version well. (Teams should share documents separately among themselves before ready to upload to github.)

## Next steps
* Wed July 28: two teams touch base. Aim to finish data tidying by then.


# Notes from Jul 27 call with Maria, Luke, Prof Bogden
Feedback from Luke:
* wants visualizations to better understand complaints, weather patterns, temps, delivery of materials - how it all interacts
* Ideally, our work will help prepare them for next phase, when oil companies are required to sample twice / year. Continuous fenceline monitoring as well as emissions testing.
* Tom Mikulka study (look at this) --> he will send info to us
* If possible, include CDC info on cancer rates and any increased risk in tank areas --> Hani: one possible issue is the recentness of the data (may be hard to say much with 2020 data only)--> DEP data may also be available that could help

Feedback from Prof:
* Don't delete data from df unless necessary
* Final presentation:- send images to PPT or readme.md file or webpage --> all that is easy. Put code in directories, then point to those directories as appropriate in a readme.md
* Maps:plotly.py: have tutorials on putting data on a map (https://plotly.com/python/scatter-plots-on-maps/
