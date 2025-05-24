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
- `cumulative_species_rasters/`: Accumulation of the current, future, and then change rasters to identify average areas of loss and gain along the coast
- `current_species_rasters/`: Habitat suitability raster files that are the result of running the ESDM with the environmental variables from 2000-2010
- `projected_species_rasters/`: Habitat suitability Raster files that are the result of running the ESDM with the projected environmental variables from 2050-2060


Each file contains the name of the intertidal species within the file name. Here is the data structure: 

```
ESDM_outputs_data
|
├── change_species_rasters/
│     ├── ESDM_Acmaea_mitra_change.tif
│     ├── ESDM_Acrosorium_ssp_change.tif
│     ├── ESDM_Ahnfeltiopsis_linearis_change.tif
│     ├── ESDM_Amphissa_columbiana_change.tif
│     ├── ESDM_Analipus_japonicus_change.tif
│     ├── ESDM_Aplysia_california_change.tif
│     ├── ESDM_Bugula_neitina_change.tif
│     ├── ESDM_Calliostoma_canaliculatum_change.tif
│     ├── ESDM_Calliostoma_ligatum_change.tif
│     ├── ESDM_Chondria_arcuata_change.tif
│     ├── ESDM_Chondria_dasyphylla_change.tif
│     ├── ESDM_Chone_minuta_change.tif
│     ├── ESDM_Cirolana_spp_Gnorimosphaeroma_oregonese_change.tif
│     ├── ESDM_Crytochiton_stelleri_change.tif
│     ├── ESDM_Cryptosiphonia_woodii_change.tif
│     ├── ESDM_Derbesia_marina_change.tif
│     ├── ESDM_Desmarestia_ligulata_change.tif
│     ├── ESDM_Dictyota_coriacea_change.tif
│     ├── ESDM_Dilsea_californica_change.tif
│     ├── ESDM_Diodora_aspera_change.tif
│     ├── ESDM_Fucus_spp_change.tif
│     ├── ESDM_Gastroclonium_parvum_change.tif
│     ├── ESDM_Halichondria_spp_change.tif
│     ├── ESDM_Halosaccion_glandiforme_change.tif
│     ├── ESDM_Halymenia_Schizymenia_spp_change.tif
│     ├── ESDM_Haminoea_vesicula_change.tif
│     ├── ESDM_Haplogloia_andersonii_change.tif
│     ├── ESDM_Henricia_spp_change.tif
│     ├── ESDM_Jania_rosea_change.tif
│     ├── ESDM_Laminaria_setchellii_change.tif
│     ├── ESDM_Laminaria_sinclairii_change.tif
│     ├── ESDM_Laurencia_spp_change.tif
│     ├── ESDM_Lottia_asmi_change.tif
│     ├── ESDM_Macron_lividus_change.tif
│     ├── ESDM_Nemalion_elminthoides_change.tif
│     ├── ESDM_Neoptilota_Ptilota_spp_change.tif
│     ├── ESDM_Neorhodomela_larix_change.tif
│     ├── ESDM_Neorhodomela_oregona_change.tif
│     ├── ESDM_Norrisia_norrisii_change.tif
│     ├── ESDM_Onchidella_carpenteri_change.tif
│     ├── ESDM_Paraxanthias_taylori_change.tif
│     ├── ESDM_Pelvetiopsis_arborescens_limitata_change.tif
│     ├── ESDM_Pseudochama_exogyra_change.tif
│     ├── ESDM_Roperia_poulsoni_change.tif
│     ├── ESDM_Sargassum_agardhianum_change.tif
│     ├── ESDM_Semibalanus_cariosus_change.tif
│     ├── ESDM_Spirobranchus_spinosus_change.tif
│     ├── ESDM_Styela_montereyensis_change.tif
│     ├── ESDM_Taonia_lennebackerae_change.tif
│     ├── ESDM_Tegula_aureotincta_change.tif
│     ├── ESDM_Tegula_brunnea_change.tif
│     ├── ESDM_Ulothrix_spp_change.tif
|     └── ESDM_Zonaria_farlowii_change.tif
|
├── cumulative_species_rasters/
│     ├──cumulative_change.tif		
│     ├──cumulative_current.tif
|     └──cumulative_projected.tif
|
├── current_species_rasters/
│     ├── current_Acmaea_mitra.tif
│     ├── current_Acrosorium_spp.tif
│     ├── current_Ahnfeltiopsis_linearis.tif
│     ├── current_Amphissa_columbiana.tif
│     ├── current_Analipus_japonicus.tif
│     ├── current_Aplysia_californica.tif
│     ├── current_Bugula_neritina.tif
│     ├── current_Calliostoma_canaliculatum.tif
│     ├── current_Calliostoma_ligatum.tif
│     ├── current_Chondria_arcuata.tif
│     ├── current_Chondria_dasyphylla.tif
│     ├── current_Chone_minuta.tif
│     ├── current_Cirolana_spp_Gnorimosphaeroma_oregonense.tif
│     ├── current_Cryptochiton_stelleri.tif
│     ├── current_Cryptosiphonia_woodii.tif
│     ├── current_Derbesia_marina.tif
│     ├── current_Desmarestia_ligulata.tif
│     ├── current_Dictyota_coriacea.tif
│     ├── current_Dilsea_californica.tif
│     ├── current_Diodora_aspera.tif
│     ├── current_Fucus_spp.tif
│     ├── current_Gastroclonium_parvum.tif
│     ├── current_Halichondria_spp.tif
│     ├── current_Halosaccion_glandiforme.tif
│     ├── current_Halymenia_Schizymenia_spp.tif
│     ├── current_Haminoea_vesicula.tif
│     ├── current_Haplogloia_andersonii.tif
│     ├── current_Henricia_spp.tif
│     ├── current_Jania_rosea.tif
│     ├── current_Laminaria_setchellii.tif
│     ├── current_Laminaria_sinclairii.tif
│     ├── current_Laurencia_spp.tif
│     ├── current_Lottia_asmi.tif
│     ├── current_Macron_lividus.tif
│     ├── current_Nemalion_elminthoides.tif
│     ├── current_Neoptilota_Ptilota_spp.tif
│     ├── current_Neorhodomela_larix.tif
│     ├── current_Neorhodomela_oregona.tif
│     ├── current_Norrisia_norrisii.tif
│     ├── current_Onchidella_carpenteri.tif
│     ├── current_Paraxanthias_taylori.tif
│     ├── current_Pelvetiopsis_arborescens_limitata.tif
│     ├── current_Pseudochama_exogyra.tif
│     ├── current_Roperia_poulsoni.tif
│     ├── current_Sargassum_agardhianum.tif
│     ├── current_Semibalanus_cariosus.tif
│     ├── current_Spirobranchus_spinosus.tif
│     ├── current_Styela_montereyensis.tif
│     ├── current_Taonia_lennebackerae.tif
│     ├── current_Tegula_aureotincta.tif
│     ├── current_Tegula_brunnea.tif
│     ├── current_Ulothrix_spp.tif
│     └── current_Zonaria_farlowii.tif
|
├── projected_species_rasters/ 
│     ├── projected_Acmaea_mitra.tif
│     ├── projected_Acrosorium_spp.tif
│     ├── projected_Ahnfeltiopsis_linearis.tif
│     ├── projected_Amphissa_columbiana.tif
│     ├── projected_Analipus_japonicus.tif
│     ├── projected_Aplysia_californica.tif
│     ├── projected_Bugula_neritina.tif
│     ├── projected_Calliostoma_canaliculatum.tif
│     ├── projected_Calliostoma_ligatum.tif
│     ├── projected_Chondria_arcuata.tif
│     ├── projected_Chondria_dasyphylla.tif
│     ├── projected_Chone_minuta.tif
│     ├── projected_Cirolana_spp_Gnorimosphaeroma_oregonense.tif
│     ├── projected_Cryptochiton_stelleri.tif
│     ├── projected_Cryptosiphonia_woodii.tif
│     ├── projected_Derbesia_marina.tif
│     ├── projected_Desmarestia_ligulata.tif
│     ├── projected_Dictyota_coriacea.tif
│     ├── projected_Dilsea_californica.tif
│     ├── projected_Diodora_aspera.tif
│     ├── projected_Fucus_spp.tif
│     ├── projected_Gastroclonium_parvum.tif
│     ├── projected_Halichondria_spp.tif
│     ├── projected_Halosaccion_glandiforme.tif
│     ├── projected_Halymenia_Schizymenia_spp.tif
│     ├── projected_Haminoea_vesicula.tif
│     ├── projected_Haplogloia_andersonii.tif
│     ├── projected_Henricia_spp.tif
│     ├── projected_Jania_rosea.tif
│     ├── projected_Laminaria_setchellii.tif
│     ├── projected_Laminaria_sinclairii.tif
│     ├── projected_Laurencia_spp.tif
│     ├── projected_Lottia_asmi.tif
│     ├── projected_Macron_lividus.tif
│     ├── projected_Nemalion_elminthoides.tif
│     ├── projected_Neoptilota_Ptilota_spp.tif
│     ├── projected_Neorhodomela_larix.tif
│     ├── projected_Neorhodomela_oregona.tif
│     ├── projected_Norrisia_norrisii.tif
│     ├── projected_Onchidella_carpenteri.tif
│     ├── projected_Paraxanthias_taylori.tif
│     ├── projected_Pelvetiopsis_arborescens_limitata.tif
│     ├── projected_Pseudochama_exogyra.tif
│     ├── projected_Roperia_poulsoni.tif
│     ├── projected_Sargassum_agardhianum.tif
│     ├── projected_Semibalanus_cariosus.tif
│     ├── projected_Spirobranchus_spinosus.tif
│     ├── projected_Styela_montereyensis.tif
│     ├── projected_Taonia_lennebackerae.tif
│     ├── projected_Tegula_aureotincta.tif
│     ├── projected_Tegula_brunnea.tif
│     ├── projected_Ulothrix_spp.tif
└──   └── projected_Zonaria_farlowii.tif

```


## METHODOLOGICAL INFORMATION

Species distribution models were developed using presence data from the [Multi-Agency Rocky Intertidal Network (MARINe)](https://marine.ucsc.edu/overview/index.html) Biodiversity Survey spanning 2000-2018. Raw survey data was processed in R to aggregate observations by species, geographic coordinates (latitude/longitude), and converted to presence records where total counts ≥1 were classified as present.

Environmental predictor variables were sourced from the [Bio-ORACLE](https://www.bio-oracle.org/) database and included sea surface temperature (thetao_mean), air temperature (tas_mean), salinity (so_mean), dissolved oxygen (o2_mean), mixed layer depth (mlotst_mean), and cloud cover (clt_mean). Historical environmental conditions were represented using 2000-2010 climatological averages, while future projections utilized 2050-2060 averages under the SSP4-6.0 emissions scenario. The spatial dimensions of the data were selected to select the state of Calfornia and the surrounding waters (bounding box: latitude 32° to 43°, longitude -126°  to -116°). Additionally, to remove data that would not be suitable habitat for intertidal species, all environmental variable rasters were clipped to a buffer along the coastline.  

Species distribution models were constructed using ensemble modeling via the R SSDM package. The ensemble approach integrated up to nine algorithms: Generalized Additive Models (GAM), Generalized Linear Models (GLM), Multivariate Adaptive Regression Splines (MARS), Classification Tree Analysis (CTA), Generalized Boosted Models (GBM), Maximum Entropy (MAXENT), Artificial Neural Networks (ANN), Random Forest (RF), and Support Vector Machines (SVM). Individual algorithms were excluded for species with insufficient observations to support model convergence.
Current and projected habitat suitability maps were generated as raster files (.tif format) at the resolution of the Bio-ORACLE environmental layers. Range shift projections were calculated by subtracting current suitability rasters from projected rasters to quantify spatial changes in habitat suitability between time periods.


