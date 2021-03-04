# The detection of Road network in the ancient Mediterranean based on quantitative analysis of inscriptions
*ANALYSIS*

---

![Project_status](https://img.shields.io/badge/status-in__progress-brightgreen "Project status logo")

## Purpose
The aim of this repository is to extract information about the road system in the ancient Mediterranean on the basis of surviving Latin and potentially also Greek inscriptions. 

**Project 1 - Milestones**

Milestone is a type of inscription on stone that was placed next to the road so the travellers could orientate themselves in the space. Milestones usually contained information on who built or paid for the reconstruction of the road, who was responsible for the maintenance and to the administrative region of which city the road belonged. The distances were usually stated in Roman miles with the typical formula 'milia passuum' (literally: thousand steps).

The location of milestones can help determine the course of the road, its date, and the spatial extent of the administrative units (cities in charge, so called 'caput viae').

The purpose of this project is to find a subset of all milestones in the EDH dataset and on the basis of the subset determine a set of rules for future epigraphers to help them classify an inscription as a milestone. 

The set of rules will contain: 

1. the most common words occuring in a milestone
1. most common material
1. typical range of physical dimensions etc.

FUTURE STEPS: The example of a milestone inscription will be later expanded to all types of inscriptions in order to create a handbook for epigraphers.

**Subproject 1 - classification of inscriptions**

Train a classification model (based on the data + metadata available through EDH dataset, 80,000+ records) to help classify an input dataset.

Training dataset - use attributes (sorted from the most important):
1. `clean_text_interpretive_word` = containing clean text of an inscription
2. `type_of_inscription_clean` = containing cleaned typology for inscriptions
3. `material_clean` = cleaned material of the inscribed object

Additional attributes that can be used to improve the classification:
5. `height_cm` = cleaned maximal height of the object
6. `width_cm` = cleaned maximal width of the object
7. `depth_cm` = cleaned maximal depth of the object
8. `type_of_monument_clean` = cleaned typology of types of inscribed objects

The input dataset has no formal typology, it contains the following attributes (link to the dataset TBA)
1. `clean_text_interpretive_word` = containing clean text of an inscription
2. `material` = cleaned material of the inscribed object

*Scenario:* 
Based on the training dataset generate a classification model that would help researchers classify inscritpions in an input dataset. 
Ideal outcome of the model - numeric representation of a probability with which an inscription X from the input dataset falls into the categorisation of inscription types. For example, inscription X from input dataset is categorised as 56 % milestone,  45 % decree,  10 % funerary inscription, 1 % list.

**Project 2 - Road use on inscriptions**

According to a widely accepted theory, inscriptions were clustered along the roads or in their proximity. Their contents were often communicating with the travellers, evidenced by the frequent use of invocations for travellers such as 'viator' or 'parodita' in the text of inscriptions. Other inscriptions mention the traffic on the roads and their use by the army or by the local communities as well. 

I have created a set of Latin vocabularies related to the use of roads, their construction and physical ammenities connected with the road traffic. I will search for the occurences of these terms in the text of the inscription in order to create a subset of inscriptions related to a road use.

I will then assess the usefulness of the method by spotchecking the text of inscriptions and the relevance of their text to the use of the road system. I will reevaluate the list of the vocabularies based on the findings.

I will analyse the frequency of topics occuring on the road related inscriptions, e.g. commercial or military traffic on the roads, individual travellers, physical ammenities, building activities etc. and compare them over space and time (by the Roman Provinces, by centuries).

As a next step, I will overlay the subset of isncriptions with the known datasets of the Roman roads (e.g. Barrington Atlas of the Greek and Roman world, Pleaides) in order to detect any spatial clusters of inscriptions away from the course of known roads. This was a new (undiscovered) Roman roads could be detected, but also the relation between roads and spatial dispositions of inscriptions can be verified.

## Authors
* Petra Hermankova [![](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-6349-0540), SDAM project, Aarhus University, petra.hermankova@cas.au.dk
 

## License
[![License: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/80x15.png "Creative Commons License CC BY-NC-SA 4.0")](https://creativecommons.org/licenses/by-nc-sa/4.0/) CC-BY-SA 4.0, see attached [License](https://github.com/sdam-au/epigraphic_roads/blob/master/LICENSE.md) 

## Data
Epigraphic dataset - Epigraphic Database Heidelberg, see a series of scripts in [EDH_ETL Repository](https://github.com/sdam-au/EDH_ETL) used to access and clean the tabular attributes of the dataset and the text of inscriptions.

### Tabular metadadata

Description of individual attributes and their source 

[EDH dataset metadata](https://docs.google.com/spreadsheets/d/1O_4EH-POKqUgq5K-B1DbbJQ8WWF0NQ6s12dCiW29MbA/edit?usp=sharing)

### Input dataset 

Public link: 

`https://sciencedata.dk/public/b6b6afdb969d378b70929e86e58ad975/EDH_text_cleaned_2021-01-21.json`

**Access with R (using custom `sdam` package)

```r
resp = request("EDH_text_cleaned_2021-01-21.json", path="/sharingin/648597@au.dk/SDAM_root/SDAM_data/EDH/public", method="GET")
```

**Access with Python (using custom [SDDK package](https://pypi.org/project/sddk/))

```python
!pip install sddk
import sddk
auth = sddk.configure("SDAM_root", "648597@au.dk") # where "648597@au.dk is owner of the shared folder, i.e. Vojtěch
EDH_utf8 = sddk.read_file("public/b6b6afdb969d378b70929e86e58ad975/EDH_text_cleaned_2021-01-21.json", "df", auth)
```

### Data output (public folder on Sciencedata.dk)

https://sciencedata.dk/shared/66cbabddae0e02c6ae6c15be9746990c

## Scripts

TBA
 










