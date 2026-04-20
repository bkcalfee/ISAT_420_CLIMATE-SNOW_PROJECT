# Dataset Description Draft

This draft summarizes what is already supported by the local project files and session handoff for the climate-snow project, and it flags the source details that still need to be confirmed before this becomes final report text.

## Datasets Used

This project currently uses three main dataset groups:

1. A short local observed Massanutten station record
2. Two Daymet point datasets for Massanutten and Harrisonburg
3. A long-term NOAA station dataset from Dale Enterprise, Virginia, used as a snowfall proxy

## 1. Local Observed Massanutten Station Dataset

Local file:
- `Data/2016-2026 22840 Daily.csv`

What the dataset covers:
- This file contains daily observations for `MASSANUTTEN 1.3 SE, VA US`
- Based on the file contents currently in the repo, the record begins on `2016-02-05`
- The session handoff describes this as a short local record covering roughly `2016-2026`

Variables involved:
- `STATION`
- `NAME`
- `DATE`
- `DAPR`
- `MDPR`
- `PRCP`
- `SNOW`
- `SNWD`

How the dataset was collected:
- Based on the file structure and station-style fields, this appears to be direct local station observation data rather than a modeled or reanalysis product
- It is being treated in the project as the on-the-ground observed record for recent Massanutten conditions

Format:
- CSV table with one row per day

How this dataset relates to the project issue:
- This dataset provides the most local and direct evidence of recent snowfall and precipitation conditions near Massanutten
- It is useful for showing what has happened on the ground in the recent period
- Its main limitation is that the time span is too short for strong long-term climate trend analysis by itself

What still needs to be confirmed:
- The exact download source or portal used to obtain this CSV
- Whether this file came directly from NOAA or from another station-data interface
- A persistent identifier or source URL, if one exists
- The exact meaning of the `DAPR` and `MDPR` fields for the report text

## 2. Daymet Point Datasets

Local files:
- `Data/daymet_massanutten.csv`
- `Data/daymet_harrisonburg.csv`

What the datasets cover:
- These files provide daily Daymet point data for two locations used in the project:
- Massanutten:
  - latitude `38.4062`
  - longitude `-78.7378`
  - elevation `509 meters`
- Harrisonburg:
  - latitude `38.4496`
  - longitude `-78.8689`
  - elevation `421 meters`
- The files indicate `All years; all variables; Daymet Software Version 4.0`
- The session handoff states that these point files cover roughly `1980-2024`

Variables involved:
- `year`
- `yday`
- `prcp (mm/day)`
- `swe (kg/m^2)`
- `tmax (deg c)`
- `tmin (deg c)`

Background and collection method:
- Daymet is a gridded daily surface weather product for North America
- In this project, the local files are point extractions rather than full gridded rasters
- Daymet should be described as a modeled/interpolated gridded climate dataset derived from observations, not as a pure direct station record
- The exact formal wording for how Daymet is generated still needs to be checked from the official documentation before finalizing the report

Format:
- CSV files with metadata header lines followed by daily tabular data

Persistent identifier already available in the file header:
- DOI: `https://doi.org/10.3334/ORNLDAAC/2129`

How these datasets relate to the project issue:
- These datasets provide the longer climate context that the short local Massanutten record cannot provide on its own
- They allow comparison between a mountain location and a nearby valley location
- They are being used to compare precipitation and temperature conditions between Massanutten and Harrisonburg
- They are also being used to evaluate how well Daymet agrees with the short observed Massanutten station record during the overlap period

What still needs to be confirmed:
- The exact download steps or URL used to obtain these point files
- Whether they were downloaded through the Daymet website, ORNL DAAC tools, NASA Earthdata search, or another interface
- The final report wording for how Daymet data are produced and quality-controlled

## 3. NOAA Dale Enterprise Daily Dataset

Local file:
- `Data/NOAA_DALE_ENTERPRISE_daily.csv`

What the dataset covers:
- This file contains daily data for:
- station id `USC00442208`
- station name `DALE ENTERPRISE, VA US`
- latitude `38.4547`
- longitude `-78.9352`
- elevation `413.9`
- The file in the repo begins on `1893-01-01`
- The session handoff states that this station provides the long-term proxy record used for snowfall and temperature analysis

Variables involved:
- `STATION`
- `NAME`
- `LATITUDE`
- `LONGITUDE`
- `ELEVATION`
- `DATE`
- `DAPR`
- `MDPR`
- `PRCP`
- `SNOW`
- `SNWD`
- `TMAX`
- `TMIN`
- `TOBS`

How the dataset was collected:
- This appears to be a direct station observation dataset rather than a modeled product
- In the project, it is being used as a long-term proxy because the local Massanutten record is too short to study long snowfall trends

Format:
- CSV table with one row per day

How this dataset relates to the project issue:
- This dataset makes it possible to analyze long-term snowfall and winter temperature relationships back into the late 19th century
- It supports the part of the project focused on long-term snowfall trends and the connection between snowfall and temperature
- The session handoff notes that earlier analysis from this station showed:
- annual snowfall trend is negative
- winter snowfall trend is negative
- snowfall is negatively correlated with warmer winter temperatures

What still needs to be confirmed:
- The exact NOAA source page or API used to download the file
- Whether the station record came from NOAA Climate Data Online, GHCN-Daily, or another NOAA access point
- A formal persistent identifier for the dataset, if one exists beyond the station id
- The exact unit conventions for each variable as downloaded, so the report can state them accurately

## Working Summary

What is already well supported by local files:
- Dataset names and local file paths
- Basic time coverage
- Core variables
- File formats
- The Daymet DOI
- The role each dataset plays in the project

What still needs outside-source confirmation before this is final:
- Exact download locations and retrieval steps
- Official background wording on how Daymet was produced
- Official background wording on the NOAA/local station data sources
- Persistent source links for the NOAA and Massanutten station files
- Unit definitions and field definitions for all NOAA-style variables

## Likely Final Framing For The Report

The report will likely describe the dataset strategy as follows:

- The short Massanutten station record provides recent on-the-ground observations
- The Daymet point datasets provide longer-term local climate context and valley-versus-mountain comparison
- The Dale Enterprise NOAA record provides the long time span needed for snowfall trend analysis

This structure matches the current workflow notebook and the prior project analysis.
