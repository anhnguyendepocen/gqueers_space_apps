### Technical Solution Details

The grading of Manageable, Moderate, and Critical comes from GIDEON's algorithm that models from 4 major variables: covid-19 growth, night light imagery, nitrogen dioxide, and human mobility. Pre-processing of the raw datasets is done to make it ready for the model.

The model made use of ordinary least squares regression from the variables. 

#### Data Preparation for Night Light Imagery (Proxy for Economic Activity)
We captured screenshots of night light from Worldview EOS. Then we processed to extract the colors (RGB values) and then took the ratio of white (light). We took the values of light intensity from HSV. Then we calculated the change in light intensity values from before and during covid-19 pandemic onset. 

### Data Preparation for GDP Data
We encoded the GDP values manually (historical) from 2018 to 2020 from Trading Economics website then plugged it in the model. 

#### Data Preparation for Nitrogen Dioxide (Environmental Impact)
With Sentinel as our main image source for offline nitrogen dioxide, the data collection started from July 2018 to the present quarter. We took quarterly screenshots and then processed to extract the colors (RGB values). We separate the R, G, and B bands. We took percent change of the three bands and plugged it in the model. 

#### Data Preparation for Human Mobility (Human Activity)
To match the other variables in the study, we aggregated the human mobility data of Google per quarter. Two quarters of data were captured. The available dataset was only from the period of the pandemic from February 15, 2020 to present day. 

#### R^2 Values
R^2 values derived from our initial run of the GIDEON model are indicative with values ranging from 0.7 to 0.9. 

#### Related Literature
1. Night-Time Light Data: A Good Proxy Measure for Economic Activity https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4619681/
2. WHO Guidelines for Indoor Air Quality: Selected Pollutants: https://www.ncbi.nlm.nih.gov/books/NBK138707/