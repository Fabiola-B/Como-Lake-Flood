# Como-Lake-Flood

The Repository contains datasets about the hydrological and meteorological triggers of lake floods, affecting the town of Como, Italy, since 1981.
For any questions regarding the data you should contact fabiola.banfi@polimi.it.

## Description of files

All files are semicolumn delimited CSV files.

### Flood characteristics

The file `flood.csv` contains information about the charcateristics of lake floods affecting the town of Como, from 1981 up to 2020. For each event it is reported: 
- the date of the flood peak (`date`);
- the peak height above the flooding threhsold in cm (`peak_cm`);
- the duration in days of the event (`duration_days`);
- the severity of the event (`severity_cm_days`)
- the date of the closest rainfall event before the flood (`date_last_rainfall`);
- a categorization of flood events (see Figure `mode.png`)

### Triggers of lake floods

The file `trigger.csv` contains information about how much each trigger contributed to the increase of water level that resulted in a a lake flood.
For each event, it is reported:
- the date of the flood peak (`date`);
- the classification in spring/autumn events (`type`);
- the total increase in level (`level_increase`), from the initial level (`initial_level`) up to the level of flood peak;
- the contribution of snow melt (`melting`), sparse rainfall events (`rainfall`), clustered rainfall events (`rainfall_cluster`) or individual rainfall events (`single rainfall`) in the increase of water level. The `last rainfall` is the increase of water level associated with the last rainfall event before the flood, this contribution is already counted in `single rainfall` or `rainfall cluster`.

### Weather circulations during lake floods

The file `WT_cluster.csv` contains information about the weather circulation types (WT) associated with lake flood events triggered by a temporal clustering of rainfall. For each event, it is reported:
- the occurrence date (`date`);
- the percentage with which each weather pattern (`WT1`, ..., `WT8`, see Salinger et al. 2015 for the definition of each WT) contributed to the increase in water lake level.

Events are sorted in order of increasing severity.


The file `WT_frequency.csv` contains the frequency (%) of each weather pattern
- for the whole series (`type = 1`),
- for days with precipitation above the 0.8 quantile of wet days (`type = 2`), 
- for days in which a raifnall event preceding a flood occured (`type = 3`).

Frequencies were computed considering the period 1981--2010.

## References
Salinger, M.J., Baldi, M., Grifoni, D. et al. Seasonal differences in climate in the Chianti region of Tuscany and the relationship to vintage wine quality. Int J Biometeorol 59, 1799–1811 (2015). https://doi.org/10.1007/s00484-015-0988-8
