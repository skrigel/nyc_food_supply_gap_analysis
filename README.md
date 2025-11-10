# This project analyzes food assistance accessibility across New York City by linking food pantry locations with census tract and neighborhood-level (NTA) socioeconomic data.

## Project Structure

```
data/                                  # Processed data to be used for anaylsis
raw/
 ├─ census_tracts.geojson              # Original source tract data
 ├─ pantries.geojson                   # Original food pantry data
aggregate_analysis.ipynb               # Spatial aggregation & tract-level analysis
merge_datasets.ipynb                   # Merge tract and NTA datasets
raw_processing.ipynb                   # Parse and clean raw GeoJSON data
```

## Worflow 

1. Raw Processing (raw_processing.ipynb)
- Cleans raw GeoJSON (tracts, pantries).
- Normalizes attributes and fixes coordinates.

2. Merging Datasets (merge_datasets.ipynb)
- Combines pantry data with NTA-level metrics.
- Joins by nta2020 code.

3. Aggregation & Analysis (aggregate_analysis.ipynb)
- Spatial join of pantries → census tracts.
- Calculates pantries per tract / per NTA
