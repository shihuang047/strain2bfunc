# strain2bfunc

## Motivations
The strain-resolved analysis is a widespread demand because the co-existence of strains with distinct functional capacities in the microbial communities indicates unique functional/metabolic capability
* Microbiome association studies: more host phenotypes can be distinguished, which can NOT be achieved at the species level or higher taxonomic ranks
* Strain-specific infection: Help physicians make accurate clinical diagnoses, relevant to bacterial resistance to infection
* Explore the transmission/translocation patterns of strain-specific microorganisms

## Key challenges
* The conventional metagenome method requires high sequencing coverage and is thus cost-prohibitive and resource-intensive.
* Low-biomass issues make strain-level microbial identification harder<img width="780" alt="image" src="https://github.com/shihuang047/strain2bfunc/assets/44211414/9c517599-872d-49d7-a303-b3cc4cb11745">


## Computation pipeline
--------------------------------
### System requirements
#### Dependencies
All scripts in 2bRAD-M are written using Perl and recommended to run in a conda environment. This program should work properly in the Unix systems, or Mac OSX, as all required packages can be appropreiately download and installed.

#### Disk space
Construction of a 2bRAD-M standard database (i.e., 2b-Tag-DB) requires approximately 10 GB of disk space.

#### Memory usage
Running the standard pipeline requires < 30Gb of RAM, which is also compatible with multithreading. For example, the BcgI-derived (default) database size is 9.32 GB, and you will need more than that in RAM if you want to build the default database. In a test early on, the peak memory can reach up to 29GB.

#### Speed
About 20 minutes are required for loading the 2b-Tag-DB. For a typical gut metagenome, ~40 minutes are required for species profiling.



## Acknowledgements
 This work is supported by XXX.

