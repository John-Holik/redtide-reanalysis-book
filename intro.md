# Red Tide Data Reanalysis

This study focuses on improving predictive modeling for harmful algal blooms, specifically red tide events in the Peace River region of Florida. The approach integrates observed environmental data with simulated model outputs to generate a reanalysis dataset using data assimilation techniques. By aligning and correcting model predictions with real-world observations, the system produces a more accurate and continuous representation of environmental conditions.

## Background

Large concentrations of Karenia brevis, a toxic mixotrophic dinoflagellate, make up the red tide along the West Florida Shelf (WFS) in the Gulf of Mexico. Besides being toxic, red tide causes unpleasant odor and scenery, which result in multiple environmental and socioeconomic impacts and public health issues. By modeling Peace River hydrological data, we can build a model that predicts harmful K.b. blooms and identifies the driving factors behind it.

## What this book contains

This book documents two parallel analyses that apply four ensemble-based uncertainty quantification methods, Bootstrap, GLUE, EnKF, and LPU, to different components of the Peace River reanalysis pipeline.

**Discharge** — The discharge analysis generates ensemble reanalysis realizations of Peace River flow using multiple UQ methods (Bootstrap, GLUE, EnKF, LPU), which matters because those realizations feed the downstream Random Forest bloom classifier as probabilistic inputs - letting the model express red tide risk as a distribution over plausible flow states rather than a single deterministic forecast..

**Total Nitrogen (TN)** — The TN analysis applies the same UQ ensemble pipeline to Total Nitrogen concentrations in the Peace River, differing from the discharge track in that TN is a sparsely-sampled water quality variable (not a continuous daily flow series), so the EDA and validation work in Phase 12 has to establish data-quality and temporal-coverage ground truth before the Bootstrap/GLUE/EnKF/LPU methods can be meaningfully applied..

Each track contains seven notebooks covering model serialization, the four UQ methods, a comparative benchmark, and ensemble-member inference into the bloom prediction model.

## How to navigate

Use the sidebar on the left to select a track, then step through the notebooks in order. Each notebook is self-contained and includes its executed outputs.

## Data sources

- USGS Station 02296750 
- USGS Station 02297330
- USGS Station 270318081593100
- FDEP Station 3556
- Manasota Regional Water Supply - PR14 & PR18
- Weekly_Interpolated CSV (https://aselshall.github.io/redtides/machineLearning/data.html)
- WAM Model - ()

## Acknowledgments

Dr. Elshall, FGCU Alumni