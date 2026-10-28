---
title: "Movement, Water, Connection: a reproducible Python connectivity workflow and field illustration for the Greater Côa Valley rewilding landscape, Portugal"
source: https://zenodo.org/records/22979020
author:
  - "[[Linda ANGULO LOPEZ]]"
published: 2026-09-26
created: 2026-10-26
description: "Landscape connectivity models are now a standard input to rewilding and restoration planning, but the usual tools assume a Julia runtime, occurrence data of good spatial quality, and a team with time to run them. Small rewilding organisations often have none of these. We present a pure-Python circuit-theory workflow applied to the Greater Côa Valley, northern Portugal, a rewilding landscape with no published boundary polygon of its own, and pair it with a field illustration practice carried out on the same ground in August 2026. Following the multi-species framework of Prima et al. (2024), ten focal species were grouped by movement medium (land, water, air). Random Forest suitability models trained on GBIF records were converted to resistance surfaces on a 100 m grid over a 10,230 km² catchment-extended study area, and current flow was solved with a `scipy.sparse` moving-window solver. We extend the framework with three penalties drawn from local evidence: (i) a recency-weighted fire penalty from MODIS burned-area data (2015 to July 2025; 10.07% of grid cells burned at least once); (ii) a distance-decayed barrier penalty from 22 field-recorded barriers, tiered by observed permeability; and (iii) a flat penalty over two UNESCO heritage areas. A direction-of-effect check confirms the barrier penalty behaves as intended (land resistance 94.0 at fully blocking against 88.6 at easily crossable barriers; water 100.0 against 22.7). The strongest combined corridor follows the lower Côa north to the Douro. Training accuracies (0.78 to 0.99) are not validation, and we say so. The three connectivity maps were redrawn for a public gallery. The field illustrations paired with them will be published during Global Artivism Month (1 November to 10 December 2026), to test whether a model can be read, and challenged, by the people who live in the valley."
tags:
  - geospatial
---
preprint

[Journal article](https://zenodo.org/search?q=&f=resource_type%3Apublication%2Binner%3Apublication-article) Open

- [ANGULO LOPEZ, Linda (Contact person) <sup>1</sup>](https://zenodo.org/search?q=metadata.creators.person_or_org.name:%22ANGULO+LOPEZ,+Linda%22)

Landscape connectivity models are now a standard input to rewilding and restoration planning, but the usual tools assume a Julia runtime, occurrence data of good spatial quality, and a team with time to run them. Small rewilding organisations often have none of these. We present a pure-Python circuit-theory workflow applied to the Greater Côa Valley, northern Portugal, a rewilding landscape with no published boundary polygon of its own, and pair it with a field illustration practice carried out on the same ground in August 2026. Following the multi-species framework of Prima et al. (2024), ten focal species were grouped by movement medium (land, water, air). Random Forest suitability models trained on GBIF records were converted to resistance surfaces on a 100 m grid over a 10,230 km² catchment-extended study area, and current flow was solved with a \`scipy.sparse\` moving-window solver. We extend the framework with three penalties drawn from local evidence: (i) a recency-weighted fire penalty from MODIS burned-area data (2015 to July 2025; 10.07% of grid cells burned at least once); (ii) a distance-decayed barrier penalty from 22 field-recorded barriers, tiered by observed permeability; and (iii) a flat penalty over two UNESCO heritage areas. A direction-of-effect check confirms the barrier penalty behaves as intended (land resistance 94.0 at fully blocking against 88.6 at easily crossable barriers; water 100.0 against 22.7). The strongest combined corridor follows the lower Côa north to the Douro. Training accuracies (0.78 to 0.99) are not validation, and we say so. The three connectivity maps were redrawn for a public gallery. The field illustrations paired with them will be published during Global Artivism Month (1 November to 10 December 2026), to test whether a model can be read, and challenged, by the people who live in the valley.

## Files

### article.pdf

<iframe title="Preview" src="https://zenodo.org/records/22979020/preview/article.pdf?include_deleted=0"></iframe>

### Files (1.1 MB)

| Name                                                                                                                  | Size   |                                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [article.pdf](https://zenodo.org/records/22979020/files/article.pdf?download=1)  md5:39f9b6d39ba88c9f90be95322620b984 | 1.1 MB | [Preview](https://zenodo.org/records/22979020/preview/article.pdf?include_deleted=0) [Download](https://zenodo.org/records/22979020/files/article.pdf?download=1) |