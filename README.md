# COVID 19 Open Data
This repository houses open datasets created by Jataware for research related to the COVID-19 response efforts.

**Disclaimer**: the datasets contained in this repository have been machine curated and are not vetted by human experts. They should be taken as representative of events that occurred on the ground, but should not be considered authoritative sources or ground truth.

## Contents

- [NPI Data](#npi-data)
	- [NPI Taxonomy](#npi-taxonomy)
	- [County NPI Data](#county-npi-data)
	- [City NPI Data](#city-npi-data)
- [Healthcare Capacity Data](#healthcare-capacity-data)
	- [State Measures](#state-measures)
	- [Global Measures](#global-measures)

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

## Healthcare Capacity Data
We have also collected data on healthcare system capacity. To accomplish this, we've relied on information extraction from open source news articles. We have attempted to automatically extract the following:

* `tests`: number of tests and/or test-kits
* `ventilators`: number of ventilators or respirators
* `beds`: number of hospital beds and/or ICU beds
* `ppe`: number of n95 masks, surgical masks, PPE

We can loosely associate these metrics with a geography based on the news article. Note that we do not perform entity resolution on the extracted metrics, so they can take a variety of types:

| Category    | Type                          | Example                             |
|-------------|-------------------------------|-------------------------------------|
| tests       | tests                         | 300 tests                           |
| tests       | test-kits                     | 300 test-kits                       |
| tests       | test kits                     | 300 test kits                       |
| tests       | COVID-19 tests                | 300 COVID-19 tests                  |
| ventilators | ventilators                   | 100 ventilators                     |
| ventilators | respirators                   | 100 respirators                     |
| beds        | hospital beds                 | 50 hospital beds                    |
| beds        | ICU beds                      | 50 ICU beds                         |
| ppe         | n95 masks                     | 1,000 n95 masks                     |
| ppe         | medical masks                 | 1,000 medical masks                 |
| ppe         | surgical masks                | 1,000 surgical masks                |
| ppe         | ppe                           | 1,000 ppe                           |
| ppe         | personal protective equipment | 1,000 personal protective equipment |

### State Measures
State-level healthcare capacity data can be found in `State-Capacity-Measures.csv`.

### Global Measures
Country-level healthcare capacity data can be found in `Global-Capacity-Measures.csv`.