# carbon-volcanics
With Ben Mather, https://ctdshub.atlassian.net/browse/PIPE-1995

Ben compiled ***Petlab_Jun2019_v8_Horomaka.xlsx*** from the [GeoRock Database](http://georoc.mpch-mainz.gwdg.de/georoc/).

I edited and cleaned up some age data in the spreadsheet.

Ben wrote a script for generating additional time-dependent grids, then provided grids.

All scripts and grids availble from Dropbox or Cloudstor: https://cloudstor.aarnet.edu.au/plus/s/vgvEqAbk381z4wi/authenticate (See Ben for password).

This repo contains scripts to merge the grids and the spreadsheet data in a pleasant flat csv file.

Each volcanic rock sample from the spreadsheet is associated with the formation location/time and correspding grid values. ***VolcanoLoader.ipynb***

This flat file can then be explored for parameter correlations and machine learning inferences. ***VolcanoExplorer.ipynb***



