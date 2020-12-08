# The detection of Road network in the ancient Mediterranean based on quantitative analysis of epigraphy
*ANALYSIS*

---

![Project_status](https://img.shields.io/badge/status-in__progress-brightgreen "Project status logo")

## Purpose
The aim of this repository is to analyse information about roads and road networks in the ancient Mediterranean on the basis of surviving Greek and Latin inscriptions. 

## Authors
* Petra Hermankova [![](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-6349-0540), SDAM project, petra.hermankova@cas.au.dk

## License
[![License: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/80x15.png "Creative Commons License CC BY-NC-SA 4.0")](https://creativecommons.org/licenses/by-nc-sa/4.0/) CC-BY-SA 4.0, see attached License.md 

## Data
Epigraphic dataset - Epigraphic Database Heidelberg, see a series of scripts in [EDH_ETL Repository](https://github.com/sdam-au/edh_workflow) used to access and clean the tabular attributes of the dataset. For details about the cleaning of the text of inscriptions, see [R_CLEANING_TEXT_INSCRIPTION.Rmd](https://github.com/sdam-au/EDH_exploration/blob/master/scripts/R_CLEANING_TEXT_INSCRIPTION.Rmd).

### Input dataset 

www.sciencedata.dk/sharingin/648597@au.dk/SDAM_root/SDAM_data/EDH/public/EDH_attrs_cleaned_2020-09-30.json

Access with R (using `sdam` package)

`resp = request("EDH_attrs_cleaned_2020-09-30.json", path="/sharingin/648597@au.dk/SDAM_root/SDAM_data/EDH/public", method="GET")`

### Software

1. R, version 4.0+
1. Jupyter Notebook, running Python 3

### Tabular metadadata

TBA 









