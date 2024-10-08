# ENSO-Antarctica
Analysis Scripts used for the publication: 

 Huguenin, M. F., Holmes, R. M., Spence, P., & England, M. H. (2024). Subsurface warming of the West Antarctic continental shelf linked to El Niño-Southern Oscillation. Geophysical Research Letters, 51, e2023GL104518. https://doi.org/10.1029/2023GL104518 
 
# Packages and Functions
I use the following main python3 ([Van Rossum and Drake, 2009](https://dl.acm.org/doi/book/10.5555/1593511)) packages which are publicly available online:

- [cartopy](https://scitools.org.uk/cartopy/docs/latest/) for creating maps ([MetOffice, 2010](https://scitools.org.uk/cartopy/docs/v0.15/citation.html))
- [numpy](https://numpy.org/) for numerical operations ([Oliphant, 2007](https://archive.org/details/NumPyBook))
- [xarray](https://xarray.pydata.org/en/stable/) for loading in and working with .nc data files ([Hoyer and Hamman, 2017](https://openresearchsoftware.metajnl.com/articles/10.5334/jors.148/))

# Analysis Scripts
- To create the perturbation experiment input files (i.e., the climatological atmospheric forcing with added ENSO-associated anomalies on top), we use the following script: [Fig1_time_series_spatial_patterns_highlighting_ENSO_teleconnection.ipynb](Fig1_time_series_spatial_patterns_highlighting_ENSO_teleconnection.ipynb). It calculates the mean spatial anomalies for each of the ACCESS-OM2 input files during the four strongest El Niño and La Niña events since 1958, scales them with the idealised time series associated with ENSO and adds them to the RYF forcing files.

# List of Main Manuscript Figures
__Fig. 1__: Experimental design of the new spin-up.
[Fig1_time_series_spatial_patterns_highlighting_ENSO_teleconnection.ipynb](Fig1_time_series_spatial_patterns_highlighting_ENSO_teleconnection.ipynb)

__Fig. 2__: Response of the West Antarctic continental shelf during the peak of El Niño and La Niña events at months 12 and 24 of the simulations.
[Fig2_response_of_West_Antarctic_shelf_to_peak_EN_and_LN_event.ipynb](Fig2_response_of_West_Antarctic_shelf_to_peak_EN_and_LN_event.ipynb)

__Fig. 3__: Time series of West Antarctic subsurface shelf temperature and heat budget terms during El Niño and La Niña simulations.
[Fig3_time_series_of_West_Antarctic_subsurface_heat_budget_and_Ekman_anomalies.ipynb](Fig3_time_series_of_West_Antarctic_subsurface_heat_budget_and_Ekman_anomalies.ipynb)

__Fig. 4__: Summary schematic of anomalous physical processes on the West Antarctic continental shelf during El Niño and La Niña events.
[Fig4_schematic_of_physical_changes_in_West_Antarctica_during_ENSO.pptx](Fig4_schematic_of_physical_changes_in_West_Antarctica_during_ENSO.pptx)

# List of Supporting Information Figures
__Fig. S1__ & __Fig. S2__: Spatial maps of sea level pressure and surface wind anomalies during the
peak of the four strongest El Niño and La Niña events since 1958. [ASL_spatial_patterns_and_winds_during_ENSO.ipynb](ASL_spatial_patterns_and_winds_during_ENSO.ipynb)

__Fig. S3__ & __Fig. S4__: Spatial maps of the atmospheric forcing fields used for the El Niño simulation in the model. [all_forcing_fields_ENFull_LNFull_spatial_maps.ipynb](all_forcing_fields_ENFull_LNFull_spatial_maps.ipynb)

__Fig. S5__: Composites of the Southern Annular Mode index during strong El Niño and La Niña events. [Same script as for Fig. 1](Fig1_time_series_spatial_patterns_highlighting_ENSO_teleconnection.ipynb)

__Fig. S6__: Spatial maps of mean sea surface temperature anomalies during the peak of four strong El
Niño and four strong La Niña events since 1958. [Same script as for Fig. 1](Fig1_time_series_spatial_patterns_highlighting_ENSO_teleconnection.ipynb)

__Fig. S7__: Model temperatures and velocities in the Amundsen Sea. [Calculating_undercurrent_strength.ipynb](Calculating_undercurrent_strength.ipynb)

__Fig. S8__: The second-order subsurface Eulerian heat budget anomalies on the West Antarctic continental (100 m - 1000 m, 150°W to 60°W) during the El Niño and La Niña simulations. [Same script as for Fig. 3](Fig3_time_series_of_West_Antarctic_subsurface_heat_budget_and_Ekman_anomalies.ipynb)

__Fig. S9__: Time series of Niño 3.4 and sea ice volume anomalies. [Same script as for Fig. 3](Fig3_time_series_of_West_Antarctic_subsurface_heat_budget_and_Ekman_anomalies.ipynb)

__Fig. S10__: Time series of the accumulated anomalous heat content on the West Antarctic continental
shelf during the El Niño and La Niña simulation. [Same script as for Fig. 3](Fig3_time_series_of_West_Antarctic_subsurface_heat_budget_and_Ekman_anomalies.ipynb)

__Fig. S11__ & __Fig. S12__: Spatial maps of atmospheric anomalies during periods when the Interdecadal Pacific Oscillation (IPO) is in a positive (negative) phase. [IPO_index_and_regression_maps_JRA55_ERA5.ipynb](IPO_index_and_regression_maps_JRA55_ERA5.ipynb)

__Fig. S13__: Model temperature evaluation with Marine Mammals Exploring the Oceans Pole to Pole project (MEOP, Treasure et al., 2017). [seal_data_comparison_from_adele.ipynb](seal_data_comparison_from_adele.ipynb) and [Model_evaluation_with_JRA55_and_SOSE.ipynb](Model_evaluation_with_JRA55_and_SOSE.ipynb)

__Fig. S14__: As in Fig. S13 but for salinities. [seal_data_salinity_comparison_from_adele.ipynb](seal_data_salinity_comparison_from_adele.ipynb)

__Fig. S15__: Model evaluation with mooring data from the Pine Island (Webber et al., 2017). [evaluating_oles_pine_island_mooring_data.ipynb](evaluating_oles_pine_island_mooring_data.ipynb)

__Fig. S16__: Sea level anomalies during the El Niño and La Niña simulations. [sea_level_anomalies_ENSO.ipynb](sea_level_anomalies_ENSO.ipynb)

# A Note on the Model Input for the Perturbation Experiments
The full forcing for the El Niño and La Niña simulations is constructed by adding for each input field the ENSO spatial patterns multiplied by the composite time series to the climatological repeat year forcing. That means, for example for the surface air temperature field during El Niño, we multiply the *tas_10m* spatial map (x,y) in [ENSOAnt_data/FigS5_All_Spatial_Maps_anoms_EN.nc](ENSOAnt_data/FigS5_All_Spatial_Maps_anoms_EN.nc) with composite time series (t), the fifth column in [ENSOAnt_data/Fig1d_Time_Series_Composite_EN.nc](ENSOAnt_data/Fig1d_Time_Series_Composite_EN.nc), and add the resulting field (t, x, y) to the repeat year forcing (t, x, y).

# Full 5 TB Model Output Data on the NCI Supercomputer Gadi
```
| Description of simulation | From where I run the simulation | Input files                      | Output stored on              |
| ------------------------- | ------------------------------- | -------------------------------- | ----------------------------- |
| Control run               | * + 01deg_jra55_ryf_Control/    | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_Control/ |
| El Niño simulation        | * + 01deg_jra55_ryf_ENFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_ENFull/  |
| "    "    "    "          |                                 | *** + forcing_mean_anoms_ENFull/ |                               |
| La Niña simulation        | * + 01deg_jra55_ryf_LNFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_LNFull/  |
| "    "    "    "          |                                 | *** + forcing_mean_anoms_LNFull/ |                               |
| Location of repeat year climatological forcing: /g/data/ua8/JRA55-do/RYF/v1-3/                                                 |
```
\* `/home/561/mv7494/`
\** `/g/data/e14/mv7494/access-om2/archive/`
\*** `/g/data/e14/mv7494/ENSOAnt_input/`


# To Do:
- clean up scripts
- upon acceptance, check final order of SI figures and update the list including the link to scripts
- upon acceptance, check all data and update metadata in the ENSOAnt_data folder
- rename scripts so they are easier to understand
- when final, push to zenodo and create doi
