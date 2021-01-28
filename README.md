# carbon-volcanics
With Ben Mather, https://ctdshub.atlassian.net/browse/PIPE-1995

Ben compiled ***Petlab_Jun2019_v8_Horomaka.xlsx*** from the [GeoRock Database](http://georoc.mpch-mainz.gwdg.de/georoc/).

I edited and cleaned up some age data in the spreadsheet.

Ben wrote a script for generating additional time-dependent grids, then provided grids.

All scripts and grids availble from Dropbox or Cloudstor: https://cloudstor.aarnet.edu.au/plus/s/vgvEqAbk381z4wi/authenticate (See Ben for password).

This repo contains scripts to merge the grids and the spreadsheet data in a pleasant flat csv file.

Each volcanic rock sample from the spreadsheet is associated with the formation location/time and correspding grid values. ***VolcanoLoader.ipynb***

This flat file can then be explored for parameter correlations and machine learning inferences. ***VolcanoExplorer.ipynb***


## Questions (from Ben's original proposal)
* (1) how much carbon is released and over what timescales?

There are 972 dated volcanic rock samples that represent an eruption event. *Some* of these have CO2 data and maybe other eruption products that could be used as a proxy for amount of carbon released. If we can pin down which products to use we may be able to answer this question, otherwise the data may be too sparse.

A quick plot of **Carbon (CO2) VS Recon Age** could be enlightening, but does not show anything too interesting. Further **XXX VS Recon Age** could also be interesting, but there is nothing conclusive from these alone.

* (2) does the provenance of carbon play a role in its liberation?

The various grids represent an amount of carbon. This question re-phrased may be - *Do the values of these grids result in an eruption?* By coregistering each of the eruption events with their underlying grid we can see if there is any correlation between carbon going down and eruption event occuring. This is done in the the two notebooks in this repo. Currently this is done as single point in time, but it may be more insightful to use the "carbon" value of the grid leading up to the eruption event (i.e cumultive subducted carbon, e.g. 20Myr before eruption), but the ages of the eruption events are also not exact, making this difficult. 
The results show the (possible) correlations of the grids and the eruption events. There is no obvious parameter. 

To build an ML model to predict whether the carbon in the lithosphere/crust/etc results in an eruption we also need a baseline measurment of what  conditions of lithosphere/crust/etc carbon does NOT result in an eruption. To do this, I generated some artifical sets of points (one method using randomised locations - good, and the other using randomised ages - too biased/not representitive of "background carbon"). We then train the model to recognise "eruptions vs baseline". 

The historgrams (diagonal) show the typical baseline vs the eruption events. Subducted sediment carbon appears to be the strongest predictor of an eruption event. All the grids are significantly more correlated to an eruption event than a random variable (Sample_ID -modified).

* (3) can this be correlated with the composition of eruption products from volcanoes at specific locations through time? 

This question may pose a problem of sparsity. There is no eruption event with all measured eruption products. 
Potentially interesting products include: 'Hf', 'Nd', 'Ni','Nd143_Nd144', 'Hf176_Hf177', '207pb_204pb'
