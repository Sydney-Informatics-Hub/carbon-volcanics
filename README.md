# carbon-volcanics
With Ben Mather, https://ctdshub.atlassian.net/browse/PIPE-1995

Ben compiled ***Petlab_Jun2019_v8_Horomaka.xlsx*** from the [GeoRock Database](http://georoc.mpch-mainz.gwdg.de/georoc/).

I edited and cleaned up some age data in the spreadsheet.

Ben wrote a script for generating additional time-dependent grids, then provided grids.

All scripts and grids availble from Dropbox or Cloudstor: https://cloudstor.aarnet.edu.au/plus/s/vgvEqAbk381z4wi/authenticate (See Ben for password).

This repo contains scripts to merge the grids and the spreadsheet data in a pleasant flat csv file.

Each volcanic rock sample from the spreadsheet is associated with the formation location/time and correspding grid values. ***VolcanoLoader.ipynb***

This flat file can then be explored for parameter correlations and machine learning inferences. ***VolcanoExplorer.ipynb***


## Questions
* (1) how much carbon is released and over what timescales?

There are 972 dated volcanic rock samples that represent an eruption event. 
Plot Carbon VS Recon Age

* (2) does the provenance of carbon play a role in its liberation?

The various grids represent an amount of carbon. Do the values of these grids result in an eruption? Plot cumultive subducted carbon (e.g. 20Myr before eruption).

* (3) can this be correlated with the composition of eruption products from volcanoes at specific locations through time? 

ML, what parameters lead to eruptions?
Potentially interesting products include: 'Hf', 'Nd', 'Ni','Nd143_Nd144', 'Hf176_Hf177'
