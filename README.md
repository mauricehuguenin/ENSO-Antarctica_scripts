# ENSO-Antarctica
Analysis Scripts and Data used for the submission: 

Huguenin, M. F., Holmes, R. M., Spence, P. and England, M. H. (2023). Subsurface warming of West Antarctic coastal waters linked to El Niño events. *Geophysical Research Letters*

# Packages and Functions
I use the following main python3 ([Van Rossum and Drake, 2009](https://dl.acm.org/doi/book/10.5555/1593511)) packages which are publicly available online:

- [cartopy](https://scitools.org.uk/cartopy/docs/latest/) for creating maps ([MetOffice, 2010](https://scitools.org.uk/cartopy/docs/v0.15/citation.html))
- [numpy](https://numpy.org/) for numerical operations ([Oliphant, 2007](https://archive.org/details/NumPyBook))
- [xarray](https://xarray.pydata.org/en/stable/) for loading in and working with .nc data files ([Hoyer and Hamman, 2017](https://openresearchsoftware.metajnl.com/articles/10.5334/jors.148/))

# Analysis Scripts


# List of Figures
__Fig. 1__: Experimental design of the new spin-up.
[creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb](creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb)

__Fig. 2__: Response of the West Antarctic continental shelf during the peak of El Niño and La Niña events at months 12 and 24 of the simulations.
[ABS_sector_map_fancy_new_run_ACCESS-OM2-01.ipynb](ABS_sector_map_fancy_new_run_ACCESS-OM2-01.ipynb)

__Fig. 3__: Time series of West Antarctic subsurface shelf temperature and heat budget terms during El Niño and La Niña simulations.
[time_series_N34_and_simulated_N34_along_with_temps.ipynb](time_series_N34_and_simulated_N34_along_with_temps.ipynb)

__Fig. 4__: Summary schematic of anomalous physical processes on the West Antarctic continental shelf during El Niño and La Niña events.
[Fig4_ENSO-Ant_schematic_the_latest.pptx](Fig4_ENSO-Ant_schematic_the_latest.pptx)

# List of Supporting Information Figures
- add figures here

# Model output data on the NCI supercomputer gadi
```
| Description of simulation | From where I run the simulation | Input files                      | Output stored on              |
| ------------------------- | ------------------------------- | -------------------------------- | ----------------------------- |
| Control run               | * + 01deg_jra55_ryf_Control/    | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_Control/ |
| El Niño simulation        | * + 01deg_jra55_ryf_ENFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_ENFull/  |
|                           |                                 | *** + forcing_mean_anoms_ENFull/ |                               |
| La Niña simulation        | * + 01deg_jra55_ryf_LNFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_LNFull/  |
|                           |                                 | *** + forcing_mean_anoms_LNFull/ |                               |
```
\* `/home/561/mv7494/`
\** `/g/data/e14/mv7494/access-om2/archive/`
\*** `/g/data/e14/mv7494/ENSOAnt_input/`

# To Do:
- clean up scripts
- add data to recreate the figures when final
- add scripts for SI figures
- push to zenodo and create doi when final
