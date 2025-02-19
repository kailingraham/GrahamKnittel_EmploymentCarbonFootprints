# U.S. Employment Carbon Footprints
## Employment Vulnerability to the Energy Transition (E-VET) tool
The E-VET tool, an open, online data visualization and exploration portal, can be used to navigate the data in this repository: https://kailingraham.github.io/ecf-vis-tool/

## Repository overview
This repository contains the output datafiles from the U.S. Employment Carbon Footprints project conducted by MIT's Center for Energy & Environmental Policy Research (CEEPR). These files represent an open dataset describing the employment vulnerability of U.S. counties as measured by their employment carbon footprint (ECF), a measure of the reliance of jobs in a county on fossil fuels. The ECFs account for emissions across all “scopes” of the energy value chain, including direct fossil fuel combustion as well as the indirect emissions that occur due to electricity consumption and the production of fossil fuels that are burnt elsewhere. The dataset covers the following sectors: agriculture, construction, manufacturing, mining, commercial sectors, and fossil-fuel power generation. These sectors account for 86% of total U.S. employment and 94% of U.S. carbon emissions outside of the transportation sector. 

## File formats
Each datafile contains data on total "effective" emissions (including direct and indirect emissions and scaled to avoid double counting across emission "scopes"), employment, population, the "passthrough rate" of emissions along the energy value chain ("rho", used to scale emissions across scopes), the effective emissions per capita, and the effective emissions per employee (i.e. the ECF). Analagous figures for "burden" are reported, which describe the social cost of these emissions using the U.S. EPA's proposed $190/metric tonne social cost of carbon. Datafiles are indexed by county---for those files that consider different sectors and/or scopes, these become secondary and tertiary indices. 

For most fields, a minimum, maximum, and average value are reported based on the range of potential passthrough rates used in the analysis. These are indicated by the suffix of the field i.e. "_min", "_max", "_avg". The average values ("_avg") are used in all CEEPR analysis from this dataset.

## File naming
- ECF_total.csv - describes the overall ECF of each county, aggregated across all covered sectors and scopes.
- ECF_sector.csv - describes the ECF across all scopes for each covered sector, for each county.
- ECF_scope1.csv - describes the ECF of each county, across all sectors, when only "Scope 1" emissions (those from direct combustion of fossil fuels) are considered.
- ECF_scope2.csv - describes the ECF of each county, across all sectors, when only "Scope 2" emissions (those associated with the consumption of electricity) are considered.
- ECF_scope3.csv - describes the ECF of each county, across all sectors, when only "Scope 3" emissions (those embedded in fossil fuels produced by the county) are considered. Note that the true definition of Scope 3 emissions includes all indirect emissions in a firm's value chain, however for the purposes of this analysis we consider only the emissions embedded in coal, oil and natural gas produced by a firm when determining its Scope 3 emissions.
- ECF_sector_scope.csv - a breakdown of ECFs for each scope within each covered sector.
- ECF_total_state.csv - describes the overall ECF of each state.
