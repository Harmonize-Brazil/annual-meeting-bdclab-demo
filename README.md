<img src="https://geodecode.com.br/wp-content/uploads/2021/12/brasildatacube.png" align="left" style="height: 65px"/>
<img src="https://earth.bsc.es/harmonize/lib/exe/fetch.php?h=250&crop=0&tok=cfb750&media=wiki:logo.png" align="right" style="height: 65px"/>

<h1 style="color:#336699; text-align: center">BDC Lab Demostration - 2024 Harmonize Annual Meeting</h1>
<hr style="border:2px solid #0077b9;">

<p style="text-align: center;">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
  </a>
  <a href="https://www.tidyverse.org/lifecycle/#maturing">
    <img src="https://img.shields.io/badge/lifecycle-maturing-blue.svg" alt="lifecycle">
  </a>
</p>

<div style="text-align: center; font-size: 90%;">
    Luana Becker da Luz <a href="https://orcid.org/0000-0002-9916-1167"><i class="fab fa-orcid" aria-hidden="true" style="color: green"></i></a>,
    Ana Paula Dal'Asta <a href="https://orcid.org/0000-0002-1286-9067"><i class="fab fa-orcid" aria-hidden="true" style="color: green"></i></a>
    <br/>
    <br/>
    Earth Observation and Geoinformatics Division, National Institute for Space Research (INPE)
    <br/>
    Avenida dos Astronautas, 1758, Jardim da Granja, São José dos Campos, SP 12227-010, Brazil
    <br/><br/>
    Contact: 
    <a href="mailto:luana.luz@inpe.br">luana.luz@inpe.br;</a>
    <a href="mailto:ana.dalasta@inpe.br">ana.dalasta@inpe.br;</a>
    <a href="mailto:miguel.monteiro@inpe.br">miguel.monteiro@inpe.br</a>
    <br/>
    <br/>
    <div style="width: 60%; margin: auto">
        <div style="text-align: center; border-style: solid; border-color: #0077b9; border-width: 1px; padding: 10px;">
            <p>
              This repository contains Jupyter notebooks codes that access collections and technologies generated and developed by EODCtHRS Harmonize Brazil. The codes compute monthly NDVI, dengue cases, rainfall and temperature data for each municipality of ROI.
            </p>
        </div>
    </div>
</div>

</br>

<p style="text-align: center;">
  • <a href="#methodology">Methodology</a> &nbsp;
  • <a href="#jupyter-notebooks">Jupyter Notebooks</a> &nbsp;
</p>

<hr style="border:2px solid #0077b9;">

## Methodology

The ROI includes 21 municipalities in the Lower Tocantins Hotspot and is shown in the image below.

<h1 style="text-align: center;">
  <img src="README_flowchart_roi.png" width="90%" style="text-align: center"/>
</h1>

### 1. Compute Health and Climate data: 
In this part, we used RSTAC client to query health and climate data on Harmonize STAC between start and end dates and then merge all GeoJSON dataframes in a single dataframe.
### 2. Compute NDVI data:
In this part, we used sits R package to query Sentinel 2 NDVI data on BDC STAC between start and end dates, aggregate each tile monthly, mosaic tiles of same month and then extract municipality mean for each month in a single dataframe.
### 3. Plot health, climate and ndvi csvs:
In this part, we opened precipitation, temperature, dengue and ndvi generated dataframes (csv files) and then ploted all monthly data in scatter plots.

<hr style="border:2px solid #0077b9;">

## Jupyter Notebooks

There are 3 main codes in this repository:

- **1. Compute Health and Climate data:** This code implements [part 1 of methodology](#1-compute-health-and-climate-data)
- **2. Compute NDVI data:** This code implements [part 2 of methodology](#2-compute-ndvi-data)
- **3. Plot health, climate and ndvi csvs:** This code implements [part 3 of methodology](#3-plot-health-climate-and-ndvi-csvs)