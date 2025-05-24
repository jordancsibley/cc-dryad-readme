This README.md file was generated on 2025-05-23 by Amanda Overbye, Ian Morris-Sibaja, Jordan Sibley, and Matteo Torres 

## GENERAL INFORMATION 

**Project Title**: Assessing Range Shifts of Coastal Species to Inform Conservation in a Key California Biogeographic Transition Zone

**Co-Author**: Amanda Overbye
- **Institution**: Bren School of Environmental Science & Management
- **Address**: Bren Hall, 2400 University of California, Santa Barbara, CA 93117
- **Email**: overbye@bren.ucsb.edu

**Co-Author**: Ian Morris-Sibaja
- **Institution**: Bren School of Environmental Science & Management
- **Address**: Bren Hall, 2400 University of California, Santa Barbara, CA 93117
- **Email**: ims@bren.ucsb.edu

**Co-Author**: Jordan Sibley
- **Institution**: Bren School of Environmental Science & Management
- **Address**: Bren Hall, 2400 University of California, Santa Barbara, CA 93117
- **Email**: jcsibley@bren.ucsb.edu

**Co-Author**: Matteo Torres
- **Institution**: Bren School of Environmental Science & Management
- **Address**: Bren Hall, 2400 University of California, Santa Barbara, CA 93117
- **Email**: matteotorres@bren.ucsb.edu

**Principal Investigator**: Dr. Erica Nielsen
- **Organization**: The Nature Conservancy in California
- **Address**: 1021 Anacapa St, Santa Barbara, CA 93101
- **Email**: erica.nielsen@tnc.org

**Co-Investigator**: Dr. Bruce Kendall
- **Institution**: Bren School of Environmental Science & Management
- **Address**: Bren Hall, 2400 University of California, Santa Barbara, CA 93117
- **Email**: kendall@bren.ucsb.edu

Date of Data Collection: 2025-04-27


## SHARING/ACCESS INFORMATION 

### Licenses/restrictions placed on the data:

The Bio-Oracle data is open-sourced with no restrictions on its use. The code that processes the rasters for our target species falls under the Mozilla Public License 2.0.

### Links to other publicly accessible locations of the data:

The [Bio Oracle website](https://www.bio-oracle.org/) provides comprehensive documentation for Bio-ORACLE's marine data layers, including detailed information about data collection methods, processing techniques, and primary data sources.

###  Links/relationships to ancillary data sets:

To predict habitat suitability of our target species from the Bio-Oracle rasters, we filter the MARINe data set for site presence of the target species and input the species data into the raster modeling methodology. More information on the MARINe data set can be found on the [database website](https://marine.ucsc.edu/).

To make a [MARINe Data Request](https://marine.ucsc.edu/explore-the-data/contact/index.html) follow this link and the provided instructions. A detailed look at our methodology can be viewed in coastalconservation technical documentation, and our workflow can be replicated by following the code in our coastalconservation dashboard [GitHub repository](https://github.com/coastalconservation/dashboard). 

### Citations:

- v3.0 Assis, J., Fernández Bejarano, S.J., Salazar, V.W., Schepers, L., Gouvêa, L., Fragkopoulou, E., Leclercq, F., Vanhoorne, B., Tyberghein, L., Serrão, E.A., Verbruggen, H., De Clerck, O. (2024) Bio-ORACLE v3.0. Pushing marine data layers to the CMIP6 Earth system models of climate change research. Global Ecology and Biogeography. [DOI: 10.1111/geb.13813](https://onlinelibrary.wiley.com/doi/abs/10.1111/geb.13813).

-  marine.ucsc.edu (2024). Coastal Biodiversity Surveys | MARINe. [online] Available at: [/contact/data-request-form](https://marine.ucsc.edu/explore-the-data/contact/data-request-form.html) [Accessed 8 Jan. 2025].


## DATA & FILE OVERVIEW 

The data folder, `ESDM_outputs_data` contains 4 folders that hold the results of the ensemble species distribution models (ESDM): 

- `change_species_rasters/`: Change detection map that is a result of the future suitability raster minus the current suitability raster. 
- `cumulative_species_rasters/`: 
- `current_species_rasters/`: Habitat suitability raster files that are the result of running the ESDM with the environmental variables from 2000-2010
- `projected_species_rasters/`: Habitat suitability Raster files that are the result of running the ESDM with the projected environmental variables from 2050-2060



## METHODOLOGICAL INFORMATION

Species distribution models were developed using presence data from the Multi-Agency Rocky Intertidal Network (MARINe) Biodiversity Survey spanning 2000-2018. Raw survey data was processed in R to aggregate observations by species, geographic coordinates (latitude/longitude), and converted to presence records where total counts ≥1 were classified as present.

Environmental predictor variables were sourced from the Bio-ORACLE database and included sea surface temperature (thetao_mean), air temperature (tas_mean), salinity (so_mean), dissolved oxygen (o2_mean), mixed layer depth (mlotst_mean), and cloud cover (clt_mean). Historical environmental conditions were represented using 2000-2010 climatological averages, while future projections utilized 2050-2060 averages under the SSP4-6.0 emissions scenario. The spatial dimensions of the data were selected to select the state of Calfornia and the surrounding waters (bounding box: latitude 32° to 43°, longitude -126°  to -116°). Additionally, to remove data that would not be suitable habitat for intertidal species, all environmental variable rasters were clipped to a buffer along the coastline.  

Species distribution models were constructed using ensemble modeling via the R SSDM package. The ensemble approach integrated up to nine algorithms: Generalized Additive Models (GAM), Generalized Linear Models (GLM), Multivariate Adaptive Regression Splines (MARS), Classification Tree Analysis (CTA), Generalized Boosted Models (GBM), Maximum Entropy (MAXENT), Artificial Neural Networks (ANN), Random Forest (RF), and Support Vector Machines (SVM). Individual algorithms were excluded for species with insufficient observations to support model convergence.
Current and projected habitat suitability maps were generated as raster files (.tif format) at the resolution of the Bio-ORACLE environmental layers. Range shift projections were calculated by subtracting current suitability rasters from projected rasters to quantify spatial changes in habitat suitability between time periods.


