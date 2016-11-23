# sg-derelict-proximity

Percent of people living within 500 metres of a derelict site.

This is an indicator using results obtained from the voluntary Scottish Vacant and Derelict Land Survey (SVDLS). This survey is run annually and data is collected from Scotland's 32 local authorities.

Derelict land (and buildings) is that which has been so damaged by development or use that it is incapable of being developed for beneficial use without rehabilitation, and which is not being used for either the purpose for which it is held, or for a use acceptable in a local plan.

To measure the number of people that live within 500m of any Derelict site, a national data set was constructed that estimated the population of each property identified as likely to be residential in Ordnance Survey's latest Address-Point data set. For each property in the Address-Point based dataset, the distance to the nearest derelict site boundary was calculated (all boundaries estimated on the basis of site centriod grid reference and overall site size). This highlights those properties within 500m of a derelict site. Those properties' estimated populations were then aggregated up by datazone to give a number for each datazone's population estimated to live within 500m of any derelict site. Each datazone's total population was controlled to equal the latest Mid-Year population estimates published by National Records of of Scotland. This indicator relates to the proportion living in proximity to any derelict site. It is not a measure of exposure.

Statistics provided by Scottish Government:  http://statistics.gov.scot/data/proximity-to-derelict-site

## License

Data is licensed under the Open Government License: http://www.nationalarchives.gov.uk/doc/open-government-licence/version/2/

## Requirements

- NodeJS
- npm

## Installation

Clone the repository

```
git clone https://github.com/EdinburghCityScope/sg-derelict-proximity.git
```

Install npm dependencies

```
cd sg-derelict-proximity
npm install
```

Run the API (from the sg-derelict-proximity directory)

```
node .
```

Converting the extracted data into loopback data.

```
node scripts/featureCollectionToLoopbackJson.js
```

Re-build data files from the statistics.gov.scot API

```
node scripts/build-data.js
```
