# strain2bfunc

## Motivations
The strain-resolved analysis is a widespread demand because the co-existence of strains with distinct functional capacities in the microbial communities indicates unique functional/metabolic capability
* Microbiome association studies: more host phenotypes can be distinguished, which can NOT be achieved at the species level or higher taxonomic ranks
* Strain-specific infection: Help physicians make accurate clinical diagnoses, relevant to bacterial resistance to infection
* Explore the transmission/translocation patterns of strain-specific microorganisms

## Key challenges
* The conventional metagenome method requires high sequencing coverage and is thus cost-prohibitive and resource-intensive.
* Low-biomass issues make strain-level microbial identification harder<img width="780" alt="image" src="https://github.com/shihuang047/strain2bfunc/assets/44211414/9c517599-872d-49d7-a303-b3cc4cb11745">


## Installation
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

### Download the pipeline

### Construct the reference strain2bfunc database (required)



## strain2bfunc pipeline tutorial
--------------------------------

### Overview

### Usage

The main script for implementing those analyses is `bin/2bRADM_Pipline.pl` in this repo. You can check out the usage by printing the help information via `perl bin/2bRADM_Pipline.pl -h`.
    
```
DESCRIPTION
We here provided a streamlined `strain2bfunc` pipeline for analyzing strain microbial compositions from the 2bRAD/shotgun metagenomics data based on the 2bRAD copy-number matrix.
USAGE

USAGE
Rscript strain_pipeline.R

PARAMETERS
-m <int> MODE, choices=c(0, 1), 0 for global strain level profiling, 1 for strain level profiling for identified species [default 0]
-l <file> The filepath of the sample list. Each line includes an input sample ID and the file path of corresponding DNA sequence data where each field should be separated by <tab>.
-a <file> The species abundance file (Required when MODE is equal to 0).
-t <int> The threshold of species abundance for strain-level identification (Required when MODE is equal to 0, default value is 0.001).
-s <file> The identified species list (Required when MODE is equal to 1).


Options:
 -l SAMPLE_LIST_FILE, --sample_list_file=SAMPLE_LIST_FILE
  Input the samples list file [Required]

 -a SPECIES_ABUNDANCE_FILE, --species_abundance_file=SPECIES_ABUNDANCE_FILE
  Input the species abundance file [Required when mode is equal to 0]

 -t THRESHOLD, --threshold=THRESHOLD
  The threshold of species abundance for strain-level identification, [Required when mode is equal to 0, default 0.001]

 -s SPECIES_LIST_FILE, --species_list_file=SPECIES_LIST_FILE
  Input the identified species list [Required when mode is equal to 1]

 -m MODE, --mode=MODE
  choices=c(0, 1), 0 for global strain level profiling, 1 for strain level profiling for identified species [default 0]

 -o OUTPUT_PATH, --output_path=OUTPUT_PATH
  Output file [default .]

 -h, --help
  Show this help message and exit

```

## Acknowledgements
 This work is supported by XXX.

