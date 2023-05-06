# CART_FCMacHT_codes
ArcGIS Toolbox to automate the CalculateField operation in ArcGIS in order to calculate Fish Community Macrohabitat Types (FCMacHT) over non-disturbed sites and European river network based on the Classification and Regression Trees model. This procedure is proposed in the article 'Over 200,000 kilometers of free-flowing river habitat is altered due to impoundments in Europe ' by Parasiewicz et al., Nature Communications (2023). The necessary data is included in dbf files. The source code of the main tools, scripts and algorithms used in this research is available under the GNU General Public License v3.0 at https://github.com/riverpiotr/FCMacHT_codes/blob/main/LICENSE. Other procedures and GIS steps (as described in Methods) were conducted manually and are therefore not part of the code repository.

The FCMacHT_Toolbox should work under ArcGIS Desktop 10.7.1 and older. 
You may need to edit the path to the source files. 
The code was writen in VB and would need to be transformed into Python script in order to run from the Python window in ArcGIS starting from version 10 of ArcGIS. In Model Builder it should work fine. 


<b><u>Files description:</b></u>

FCMacHT_Toolboxes.tbx - toolbox of ArcGIS containng two tools:

  20230506_Model_CalculateFiled_NDS_FCMacHT, toolbox calculating FCMacHT for NDS sites provided in NDS_attr.dbf
  
  20230506_Model_CalculateFiled_riv_FCMacHT, toolbox calculating FCMacHT for river segments provided in riv_attr.dbf
  
NDS_attr.dbf, broad environemntal attributes used to calculate FCMacHT for NDS sites

rive_attr.dbf, broad environemntal attributes used to calculate FCMacHT for river segments



<b><u>Field description of .dbf files:</b></u>


WSO1_ID,	Riversegment identifier as in CCM dataset

W_CATCH,	Catchment size upstream a given riversegment, derived from CCM dataset

W_SLOPE,	Slope of river segment, derived from CCM dataset

W_STRAHL,	Strahler stream order of river segment, derived from CCM dataset

W_ALT,	Mean altitude of riversegment, derived from CCM dataset

Z_GEO3_SI,	Geology of immediate catchment of riversegment classified as siliceaous (1,0 values), derrived from IHME1500 v 1.2

Z_GEO3_CA,	Geology of immediate catchment of riversegment classified as calcareous (1,0 values), derrived from IHME1500 v 1.2

Z_GEO3_OR,	Geology of immediate catchment of riversegment classified as organic (1,0 values), derrived from SGDB v 2.0

EnZ_01ALN,	Environmental Zone of immediate catchment of riversegment based on EnZ - Alpine North zone (1,0 values)

EnZ_02BOR,	Environmental Zone of immediate catchment of riversegment based on EnZ - Boreal zone (1,0 values)

EnZ_03NEM,	Environmental Zone of immediate catchment of riversegment based on EnZ - Nemoral zone (1,0 values)

EnZ_04ATN,	Environmental Zone of immediate catchment of riversegment based on EnZ - Atlantic North zone (1,0 values)

EnZ_05ALS,	Environmental Zone of immediate catchment of riversegment based on EnZ - Atlantic South zone (1,0 values)

EnZ_06CON,	Environmental Zone of immediate catchment of riversegment based on EnZ - Continental zone (1,0 values)

EnZ_07ATC,	Environmental Zone of immediate catchment of riversegment based on EnZ - Atlantic Central zone (1,0 values)

EnZ_08PAN,	Environmental Zone of immediate catchment of riversegment based on EnZ - Pannonian zone (1,0 values)

EnZ_09LUS,	Environmental Zone of immediate catchment of riversegment based on EnZ - Lusitanian zone (1,0 values)

EnZ_10ANA,	Environmental Zone of immediate catchment of riversegment based on EnZ - Anatolian zone (1,0 values)

EnZ_11MDM,	Environmental Zone of immediate catchment of riversegment based on EnZ - Mediterranean Mountains zone (1,0 values)

EnZ_12MDN,	Environmental Zone of immediate catchment of riversegment based on EnZ - Mediterranean North zone (1,0 values)

EnZ_13MDS,	Environmental Zone of immediate catchment of riversegment based on EnZ - Meaditerranean South zone (1,0 values)

FCMacHT,	Calculated Fish Community Macrohabitat Type 



<b><u>Underlying spatial datasets:</b></u>


CCM: De Jager, A. & Vogt, J. Rivers and Catchments of Europe - Catchment Characterisation Model (CCM). [dataset]. (European Commission, Joint Research Centre (JRC), 2007).

IHME1500: BgR & UNESCO. International Hydrogeological Map of Europe 1:1,500,000 (IHME1500). Digital map data v1.2. (Federal Institute for Geosciences and Natural Resources (BGR), 2019).

SGDB: Soil Geographical Database of Eurasia at scale 1:000,000 version 4 beta [dataset]. in The European Soil Database distribution version 2.0, CD-ROM vol. EUR 19945 EN (European Commission, 2004).

EnZ: Metzger, M. J. The Environmental Stratification of Europe [dataset]. (University of Edinburg, 2018).


