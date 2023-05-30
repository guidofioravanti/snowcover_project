# snowcover_project

A description of the steps needed for the development of snow masks for the Combined Drought Indicator.

## Introduction

The paper of [Richiardi et al.](https://www.mdpi.com/2072-4292/13/10/1957) originally uses L1C Sentinel-2 data. 

These data need:
  - atmospheric and topographic correction using  the pre-processor [Sen2Cor](https://step.esa.int/main/snap-supported-plugins/sen2cor/) (the pre-processor ouput is L2A data)
  - cloud mask extraction (using the FMASK software)

Richiardi and Adamo propose to: 
  - **skip** the atmospheric correction (Sen2Cor)
  - use the L2A data available through the [Open Access Hub](https://sentinel.esa.int/web/sentinel/sentinel-data-access)
  - apply Fmask
  - apply rLIS (revised version of the Let It Snow algorithm)

## Snow Masks 

- Sentinel-2 L2A data retrieving: 
  - BDAP for operational snow masks production
  - [R package sen2r](https://sen2r.ranghetti.info/) for quick case study development 
- Improvement of the rLIS code for its application on the European domain (in collaboration with IIA - Institute of Atmospheric Pollution Research):
  - fix the code parameters (e.g., snow altitude)
  - fix the algorithm for turbid waters
  - test the algorithm over tiles where there is no snow
  - test the algoithm against observational data  

## CDI

- Review the Combined Drought Indicator framework for including snow masks:
  - in presence of snow, the CDI should return "NO DATA"? Assess only Watch alerts? 

## Input Data

- Sentinel L2A data
- Digital Elevation Model for Europe ([EU-DEM](https://land.copernicus.eu/imagery-in-situ/eu-dem/eu-dem-v1.1))

## Case Study

- Case study for a first development of Combined Drought Indicator:
  - develop a first snow masks set for Europe (Scandinavia?) in order to test the original version of the Let It Snow algorithm described in [Richiardi et al.](https://www.mdpi.com/2072-4292/13/10/1957)

## Software

- Fmask: for cloud extraction (Command Line Interface/python/R library)
- Review the [rLIS code](https://github.com/chiararik/rLIS_VLab) (fix the parameters if needed)
- Translate the code from R to Python





  
  
  
