# ENSO-Antarctica
Analysis Scripts and Data used for the submission: 

Huguenin, M. F., Holmes, R. M., Spence, P. and England, M. H. (2023). Subsurface warming of the West Antarctic continental shelf linked to El Niño-Southern Oscillation. Submitted to *Geophysical Research Letters*.

# Packages and Functions
I use the following main python3 ([Van Rossum and Drake, 2009](https://dl.acm.org/doi/book/10.5555/1593511)) packages which are publicly available online:

- [cartopy](https://scitools.org.uk/cartopy/docs/latest/) for creating maps ([MetOffice, 2010](https://scitools.org.uk/cartopy/docs/v0.15/citation.html))
- [numpy](https://numpy.org/) for numerical operations ([Oliphant, 2007](https://archive.org/details/NumPyBook))
- [xarray](https://xarray.pydata.org/en/stable/) for loading in and working with .nc data files ([Hoyer and Hamman, 2017](https://openresearchsoftware.metajnl.com/articles/10.5334/jors.148/))

# Analysis Scripts
- To create the perturbation experiment input files (i.e., the climatological atmospheric forcing with added ENSO-associated anomalies on top), we use the following script: [creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb](creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb). It calculates the mean spatial anomalies for each of the ACCESS-OM2 input files during the four strongest El Niño and La Niña events since 1958, scales them with the idealised time series associated with ENSO and adds them to the RYF forcing files.


# List of Main Manuscript Figures
__Fig. 1__: Experimental design of the new spin-up.
[creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb](creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb)

__Fig. 2__: Response of the West Antarctic continental shelf during the peak of El Niño and La Niña events at months 12 and 24 of the simulations.
[ABS_sector_map_fancy_new_run_ACCESS-OM2-01.ipynb](ABS_sector_map_fancy_new_run_ACCESS-OM2-01.ipynb)

__Fig. 3__: Time series of West Antarctic subsurface shelf temperature and heat budget terms during El Niño and La Niña simulations.
[time_series_N34_and_simulated_N34_along_with_temps.ipynb](time_series_N34_and_simulated_N34_along_with_temps.ipynb)

__Fig. 4__: Summary schematic of anomalous physical processes on the West Antarctic continental shelf during El Niño and La Niña events.
[Fig4_ENSO-Ant_schematic_the_latest.pptx](Fig4_ENSO-Ant_schematic_the_latest.pptx)

# List of Supporting Information Figures
__Fig. S1__ & __Fig. S2__: Model evaluation with Southern Ocean State Estimate (SOSE, Verdy & Mazloff, 2017) and Marine Mammals Exploring the Oceans Pole to Pole project (MEOP, Treasure et al., 2017). [Model_evaluation_with_JRA55_and_SOSE.ipynb](Model_evaluation_with_JRA55_and_SOSE.ipynb)

__Fig. S3__ & __Fig. S4__: Spatial maps of sea level pressure and surface wind anomalies during the
peak of the four strongest El Niño and La Niña events since 1958. [ASL_spatial_patterns_and_winds_during_ENSO.ipynb](ASL_spatial_patterns_and_winds_during_ENSO.ipynb)

__Fig. S5__ & __Fig. S6__: Spatial maps of the atmospheric forcing fields used for the El Niño simulation in the model. [all_forcing_fields_ENFull_LNFull_spatial_maps.ipynb](all_forcing_fields_ENFull_LNFull_spatial_maps.ipynb)

__Fig. S7__: Composites of the Southern Annular Mode index during strong El Niño and La Niña events. [Same script as for Fig. 1](creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb)

__Fig. S8__: Time series and spatial maps of sea surface temperature anomalies. [Same script as for Fig. 1](creating_enso_sam_forcing_fields_for_ncfile_ACCESS-OM2-01_rescaled.ipynb)

__Fig. S9__: Advective heat flux anomalies on the West Antarctic continental shelf (100 m - 1000 m, 150°W to 60°W) during the El Niño and La Niña simulations. [Same script as for Fig. 3](time_series_N34_and_simulated_N34_along_with_temps.ipynb)

__Fig. S10__: Time series of Bellingshausen Sea ice volume anomalies above the continental shelf break at 1000 m depth during the El Niño and La Niña simulations. [Same script as for Fig. 3](time_series_N34_and_simulated_N34_along_with_temps.ipynb)

__Fig. S11__: Time series of West Antarctic continental shelf temperature changes and heat budget terms during the El Niño followed by La Niña simulation. [Same script as for Fig. 3](time_series_N34_and_simulated_N34_along_with_temps.ipynb)

__Fig. S12__: Time series of Niño 3.4 and sea ice volume anomalies. [Same script as for Fig. 3](time_series_N34_and_simulated_N34_along_with_temps.ipynb)

References:
- Verdy, A. and Mazloff, M. R. (2017), A data assimilating model for estimating Southern Ocean biogeochemistry, J. Geophys. Res. Oceans, 122, 6968– 6988, doi:10.1002/2016JC012650. 
- Treasure, A.M., F. Roquet, I.J. Ansorge, M.N. Bester, L. Boehme, H. Bornemann, J.-B. Charrassin, D. Chevallier, D.P. Costa, M.A. Fedak, C. Guinet, M.O. Hammill, R.G. Harcourt, M.A. Hindell, K.M. Kovacs, M.-A. Lea, P. Lovell, A.D. Lowther, C. Lydersen, T. McIntyre, C.R. McMahon, M.M.C. Muelbert, K. Nicholls, B. Picard, G. Reverdin, A.W. Trites, G.D. Williams, and P.J.N. de Bruyn. (2017), Marine Mammals Exploring the Oceans Pole to Pole: A review of the MEOP consortium. Oceanography 30(2):132–138, doi:10.5670/oceanog.2017.234.


# Full 5 TB Model Output Data on the NCI Supercomputer Gadi
```
| Description of simulation | From where I run the simulation | Input files                      | Output stored on              |
| ------------------------- | ------------------------------- | -------------------------------- | ----------------------------- |
| Control run               | * + 01deg_jra55_ryf_Control/    | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_Control/ |
| El Niño simulation        | * + 01deg_jra55_ryf_ENFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_ENFull/  |
| "    "    "    "          |                                 | *** + forcing_mean_anoms_ENFull/ |                               |
| La Niña simulation        | * + 01deg_jra55_ryf_LNFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_LNFull/  |
| "    "    "    "          |                                 | *** + forcing_mean_anoms_LNFull/ |                               |
```
\* `/home/561/mv7494/`
\** `/g/data/e14/mv7494/access-om2/archive/`
\*** `/g/data/e14/mv7494/ENSOAnt_input/`


# To Do:
- clean up scripts
- check again the final order of SI figures and update the list including the link to scripts
- add Data folder with data to recreate the figures when final
- rename scripts so they are easier to understand
- when final, push to zenodo and create doi
