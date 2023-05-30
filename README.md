# snowcover_project

A description of what steps we need to carry out to develop snow masks for CDI.

## Input data

The paper of [Richiardi et al.](https://www.mdpi.com/2072-4292/13/10/1957) originally uses L1C Sentinel-2 data. These data need:
- atmospheric and topographic correction using  "Sen2Cor" (ouput: L2A data)
- cloud mask extraction (using FMASK)

Richiardi and Adamo propose to **skip** the atmospheric correction (Sen2Cor) and use the L2A data available through the [Open Access Hub](https://sentinel.esa.int/web/sentinel/sentinel-data-access).

## Snow Masks 

- Sentinel-2 L2A data retrieving: 
  - BDAP for operational snow masks production
  - sen2r for case study development 
- Snow mask case study for the North of Europe using the rLIS (Let It Snow) algorithm described in [Richiardi et al.](https://www.mdpi.com/2072-4292/13/10/1957)
- Improvement of the rLIS code for its application on the European domain:
  - to be discussed with IIA (Institute of Atmospheric Pollution Research)  

## CDI

- Review the Combined Drought Indicator framework for including snow masks
- Case study for a first development of Combined Drought Indicator:
  - develop a first snow masks set for Europe (Scandinavia?) in order to test the original version of the Let It Snow algorithm

## Software

- Fmask: for cloud extraction (Command Line Interface/python/R library)
- Review the [rLIS code](https://github.com/chiararik/rLIS_VLab) (fix the parameters if needed)
- Translate the code from R to Python

## Datasets

- Sentinel L2A data
- Digital Elevation Model for Europe ([EU-DEM](https://land.copernicus.eu/imagery-in-situ/eu-dem/eu-dem-v1.1))




  
  
  
