# Dataset Description Draft

This project uses three dataset groups: a short local Massanutten station record, Daymet point data for Massanutten and Harrisonburg, and a long-term NOAA station record from Dale Enterprise, Virginia.

## Local Massanutten Station

Project file:
- `Data/2016-2026 22840 Daily.csv`

GitHub location:
- `https://github.com/bkcalfee/ISAT_420_CLIMATE-SNOW_PROJECT/blob/main/Data/2016-2026%2022840%20Daily.csv`

Current draft:
- This dataset is the short local observation record for `MASSANUTTEN 1.3 SE, VA US`.
- The file begins on `2016-02-05`, and the project has treated it as a recent record covering roughly `2016-2026`.
- Variables in the CSV include `DATE`, `PRCP`, `SNOW`, and `SNWD`, along with station metadata fields.
- The station id in the file is `US1VARH0011`.
- The `US1` station-id prefix is used for CoCoRaHS stations included in GHCN-Daily, which suggests this record is a volunteer observer station record distributed through the NOAA daily summaries system.
- The file format is CSV with one row per day.
- In the project, this dataset is used to represent recent on-the-ground snowfall and precipitation conditions at Massanutten.
- Its main limitation is that the record is too short for strong long-term climate trend analysis by itself.


## Daymet Point Data

Project files:
- `Data/daymet_massanutten.csv`
- `Data/daymet_harrisonburg.csv`

GitHub locations:
- `https://github.com/bkcalfee/ISAT_420_CLIMATE-SNOW_PROJECT/blob/main/Data/daymet_massanutten.csv`
- `https://github.com/bkcalfee/ISAT_420_CLIMATE-SNOW_PROJECT/blob/main/Data/daymet_harrisonburg.csv`

Current draft:
- These files provide daily Daymet point data for Massanutten and Harrisonburg.
- The Massanutten file header lists latitude `38.4062`, longitude `-78.7378`, and elevation `509 meters`.
- The Harrisonburg file header lists latitude `38.4496`, longitude `-78.8689`, and elevation `421 meters`.
- These files are point extracts from `Daymet: Daily Surface Weather Data on a 1-km Grid for North America, Version 4 R1`.
- For continental North America, the official temporal coverage is `1980-2024`, which matches the project use of these files as the longer climate-context datasets.
- The full Daymet daily product includes `tmin`, `tmax`, `prcp`, `srad`, `vp`, `swe`, and `dayl`.
- The local point files used in this project include `year`, `yday`, `prcp (mm/day)`, `swe (kg/m^2)`, `tmax (deg c)`, and `tmin (deg c)`.
- ORNL DAAC states that Daymet provides long-term, continuous gridded estimates by interpolating and extrapolating ground-based observations through statistical modeling techniques.
- In the project, these datasets are used to compare mountain versus valley climate and to compare Daymet against the short observed Massanutten record during the overlap period.



## NOAA Dale Enterprise Station

Project file:
- `Data/NOAA_DALE_ENTERPRISE_daily.csv`

GitHub location:
- `https://github.com/bkcalfee/ISAT_420_CLIMATE-SNOW_PROJECT/blob/main/Data/NOAA_DALE_ENTERPRISE_daily.csv`

Current draft:
- This dataset is the long-term proxy record used for snowfall and temperature analysis.
- The file is for station `USC00442208`, `DALE ENTERPRISE, VA US`.
- The header lists latitude `38.4547`, longitude `-78.9352`, and elevation `413.9`.
- The local file begins on `1893-01-01`.
- Variables include `PRCP`, `SNOW`, `SNWD`, `TMAX`, `TMIN`, and `TOBS`, along with station metadata fields.
- This means the Dale Enterprise file can be described as NOAA Climate Data Online daily station data from the GHCN-Daily dataset rather than as a modeled product.
- The file format is CSV with one row per day.
- In the project, this dataset is used because the local Massanutten record is too short for long-term snowfall trend analysis.


## Short Summary

- The local Massanutten station file provides recent local observations.
- The Daymet point files provide longer-term mountain-versus-valley climate context.
- The Dale Enterprise NOAA file provides the long time span needed for snowfall trend analysis.

