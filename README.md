# COVID 19 Open Data
This repository houses open datasets created by Jataware for research related to the COVID-19 response efforts.

**Disclaimer**: the datasets contained in this repository have been machine curated and are not vetted by human experts. They should be taken as representative of events that occurred on the ground, but should not be considered authoritative sources or ground truth.

## NPI Data
[Nonpharmaceutical Interventions](https://www.cdc.gov/nonpharmaceutical-interventions/index.html), or NPIs, are policy actions taken by communities to mitigate the spread of diseases such as COVID-19. These types of interventions include implementing stay at home orders, school closures, and social distancing recommendation, etc.

We have an ongoing project to scan the internet for news articles the feature country, state, county, and city level reporting on NPIs. We then categorize the NPI that the article is most likely describing in order to generate an estimate for when various NPIs were implemented and where.

### NPI Taxonomy

* `state_of_emergency`: the geography has implemented a state of emergency
* `shelter_in_place`: the geography has implemented a shelter in place or stay home order
* `lockdown`: the geography has implemented a curfew or lockdown
* `quarantine`: the geography has insituted some type of quarantine measure
* `social_distance`: the geography has required social distancing measures
* `disaster_declaration`: the geography has issued a disaster declaration
* `school_business_closure`: the geography has ordered schools or businesses to close
* `travel`: the geography has implemented travel restrictions

### County NPI Data
U.S. County level NPI data is available in `County-NPIs.csv`.

### City NPI Data
U.S. city level NPI data is available in `City-NPIs.csv`.