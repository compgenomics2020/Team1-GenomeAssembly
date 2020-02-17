# Genome Assembly Pipeline
This pipeline is designed to automate the assembly of a genome with the option to perform quality control measures and allows the user to pick between the MaSuRCa or Unicycler assemblers or the auto option, which will decide for the user based on quality metrics such as the total length of the assembled genome and N50.

* [Team 1 Genome Assembly ](#Team-1-Genome-Assembly)
* [Software Requirements](#Software-Requirements)
* [Usage](#Usage)
* [References](#References)

## Team 1- Genome Assembly
The Genome Assembly group members for Team 1 are: 
  * Cecilia (Hyeonjeong) Cheon
  * Devishi Kesar
  * Laura Mora
  * Lawrence McKinney
  * Jessica Mulligan
  * Heather Patrick

## Software Requirements
1. [fastp](https://github.com/OpenGene/fastp) (if performing read quality assessment and trimming)
2. [MaSuRCa](https://github.com/alekseyzimin/masurca) (if choosing MaSuRCa or the auto option for performing genome assembly)
3. [Unicycler](https://github.com/rrwick/Unicycler) (if choosing Unicycler or the auto option for performing genome assembly)
4. [Quast](https://github.com/ablab/quast) (tool for quality control metrics)

## Usage
INCLUDE INFO ABOUT CONFIG FILE
```
./run_genome_assembly_pipeline.sh [-t <int>] -p <dir_path> -o <dir_name> [-q] -g <m|u|a> [-v] [-h]
    -t    number of threads; default is 4
    -p    path to directory containing gzipped fastq forward and backward reads
    -o    path to output directory
    -q    perform quality control and trimming using fastp
    -g    assembler of choice; can pick between MaSuRCa, Unicycler, or auto (pipeline will run both and pick the best option)
    -v    activate verbose mode
    -h    print usage information    
```

## References
* Shifu Chen, Yanqing Zhou, Yaru Chen, Jia Gu; fastp: an ultra-fast all-in-one FASTQ preprocessor, Bioinformatics, Volume 34, Issue 17, 1 September 2018, Pages i884–i890, https://doi.org/10.1093/bioinformatics/bty560
* Zimin AV, Marçais G, Puiu D, Roberts M, Salzberg SL, Yorke JA. The MaSuRCA genome assembler. Bioinformatics. 2013 Nov 1;29(21):2669-77.
* Wick RR, Judd LM, Gorrie CL, Holt KE (2017) Unicycler: Resolving bacterial genome assemblies from short and long sequencing reads. PLoS Comput Biol 13(6): e1005595. https://doi.org/10.1371/journal.pcbi.100559

