# pipeAIRR


pipeAIRR is a community resource for adaptive immune receptore repertoire sequencing (AIRR-seq) processing pipelines.

The pipelines are implemented with [DolphinNext](https://dolphinnext.readthedocs.io/en/latest/index.html#).

We have devided the pipelines into two main sections:
1. Pre-processing
2. Downstream analysis

##  Repository layout

In each section directory you can find each of the pipelines directories containing the dolphinnext pipeline (XX.dn) as well as the configurations and the nextflow script (XX.nf)


## Frequent questions and guides

We created a small website with frequent questions, guides, and link to relavent information from DolphinNext. 

Please visit the [site](https://pipeairr.github.io/pipeAIRR/) to see our guides. 

## Pre-processing

In this section you can find pipelines to process the sequencer output files, meaning from 'raw reads' into an aligner ready fasta file.

The pipeplines were build based on the [immcantation](https://immcantation.readthedocs.io/en/stable/) framework and spesificly the [pRESTO](https://presto.readthedocs.io/) tool suite.

### Available pipelines:


| Pipeline       | Input data | Sequencing protocol | UMI        | Published paper(s)                      | GitHub Archive        |
|-----------------------|---------------------|------------------------------|---------------------|--------------------------------------------------|--------------------------------|
| RP1 | Raw  sequences           | 2X250      | +    | [11]              | [pipeAIRR/RP1](https://github.com/pipeAIRR/RP1) |
| RP2 | Raw  sequences                 | 2X250      | - | [4] | [pipeAIRR/RP2](https://github.com/pipeAIRR/RP2) |
| RP3 | Raw  sequences                 | 5' RACE                      | + |  [3], [1]      | [pipeAIRR/RP3](https://github.com/pipeAIRR/RP3) |
| RP4 | Raw  sequences                 | 2X300      | + | [2]         | [pipeAIRR/RP4](https://github.com/pipeAIRR/RP4) |
| RP5 | Raw  sequences                 | 5' RACE                      | + | [9]       | [pipeAIRR/RP5A](https://github.com/pipeAIRR/RP5A),[pipeAIRR/RP5B](https://github.com/pipeAIRR/RP5B)                 |
| RP6 | Raw  sequences                 | Roche 454                    | -  | [5]        | [pipeAIRR/RP6](https://github.com/pipeAIRR/RP6)  |
| RP7 | Raw  sequences                 | 2X125 CD4                    | -  | [8]       | [pipeAIRR/RP7](https://github.com/pipeAIRR/RP7)  |


## Downstream analysis

In this section you can find pipelines to analyze processed reads and infer genotype and haplotype.
The pipeplines were build based on the [Yaari lab framework](https://hub.docker.com/repository/docker/peresay/suite), that contains tools from:
- [immcantaton](https://immcantation.readthedocs.io/en/stable/)
- [VDJbase](vdjbase.org)
- [TIgGER](https://tigger.readthedocs.io/en/stable/)
- [RAbHIT](https://yaarilab.bitbucket.io/RAbHIT/)
- [PIgLET](https://yaarilab.github.io/IGHV_reference_book/piglet_package.html)

### Available pipelines:

| Pipeline       | Input data | Sequencing protocol | UMI        | Published paper(s)                      | GitHub Archive        |
|-----------------------|---------------------|------------------------------|---------------------|--------------------------------------------------|--------------------------------|
| PP1  | Processed sequences | -           | -  | [10]        | [pipeAIRR/PP1](https://github.com/pipeAIRR/PP1)  |
| PP2  | Processed sequences | -           | -  | [6]         | [pipeAIRR/PP2](https://github.com/pipeAIRR/PP2)  |
| PP3 | Processed sequences | -           | -  | [7]     | [pipeAIRR/PP3](https://github.com/pipeAIRR/PP3) |

## Citations:

[1] Sivan Eliyahu, Oz Sharabi, Shiri Elmedvi, Reut Timor, Ateret Davidovich, Francois Vigneault, Chris Clouser, Ronen Hope, Assy Nimer, Marius Braun, Yaacov Y. Weiss, Pazit Polak, Gur Yaari, and Meital Gal-Tanamy. Antibody repertoire analysis of hepatitis c virus infections identifies immune signatures associated with spontaneous clearance. Frontiers in Immunology, 9:3004, 2018

[2] Jacob D Galson, Sebastian Schaetzle, Rachael JM Bashford-Rogers, Matthew IJ Ray-313 bould, Aleksandr Kovaltsuk, Gavin J Kilpatrick, Ralph Minter, Donna K Finch, Jorge314 Dias, Louisa K James, et al. Deep sequencing of b cell receptor repertoires from covid-315 19 patients reveals strong convergent immune signatures. Frontiers in immunology,316 11:605170, 2020.

[3] Moriah Gidoni, Omri Snir, Ayelet Peres, Pazit Polak, Ida Lindeman, Ivana Mikocziova, Vikas Kumar Sarna, Knut EA Lundin, Christopher Clouser, Francois Vigneault, et al. Mosaic deletion patterns of the human antibody heavy chain gene locus shown by bayesian haplotyping. Nature communications, 10(1):1–14, 2019

[4] Victor Greiff, Ulrike Menzel, Ulrike Haessler, Skylar C Cook, Simon Friedensohn, Tarik A Khan, Mark Pogson, Ina Hellmann, and Sai T Reddy. Quantitative assessment of the robustness of next-generation sequencing of antibody variable gene repertoires from immunized mice. BMC immunology, 15:1–14, 2014.

[5] Ning Jiang, Jiankui He, Joshua A Weinstein, Lolita Penland, Sanae Sasaki, Xiao-Song He, Cornelia L Dekker, Nai-Ying Zheng, Min Huang, Meghan Sullivan, et al. Lineage structure of the human antibody repertoire in response to influenza vaccination. Science translational medicine, 5(171):171ra19–171ra19, 2013

[6] Aviv Omer, Or Shemesh, Ayelet Peres, Pazit Polak, Adrian J Shepherd, Corey T Watson, Scott D Boyd, Andrew M Collins, William Lees, and Gur Yaari. Vdjbase: an adaptive immune receptor genotype and haplotype database. Nucleic acids research, 48(D1):D1051–D1056, 2020

[7] Ayelet Peres, William D Lees, Oscar L Rodriguez, Noah Y Lee, Pazit Polak, Ronen Hope, Meirav Kedmi, Andrew M Collins, Mats Ohlin, Steven H Kleinstein, Corey T Watson, and Gur Yaari. IGHV allele similarity clustering improves genotype inference from adaptive immune receptor repertoire sequencing data. Nucleic Acids Research, page gkad603, 08 2023.

[8] Teresa Rubio, Maria Chernigovskaya, Susanna Marquez, Cristina Marti, Paula Izquierdo-Altarejos, Amparo Urios, Carmina Montoliu, Vicente Felipo, Ana Conesa, Victor Greiff, et al. A nextflow pipeline for t-cell receptor repertoire reconstruction and analysis from rna sequencing data. ImmunoInformatics, 6:100012, 2022.

[9] Modi Safra, Zvi Tamari, Pazit Polak, Shachaf Shiber, Moshe Matan, Hani Karameh, Yigal Helviz, Adva Levy-Barda, Vered Yahalom, Avi Peretz, et al. Altered somatic hypermutation patterns in covid-19 patients classifies disease severity. Frontiers in Immunology, 14:1031914, 2023.13

[10] Modi Safra, Lael Werner, Ayelet Peres, Pazit Polak, Naomi Salamon, Michael Schvimer, Batia Weiss, Iris Barshack, Dror S Shouval, and Gur Yaari. A somatic hypermutation based machine learning model stratifies individuals with crohn’s disease and controls. Genome Research, 33(1):71–79, 2023

[11] Joel NH Stern, Gur Yaari, Jason A Vander Heiden, George Church, William F Donahue, Rogier Q Hintzen, Anita J Huttner, Jon D Laman, Rashed M Nagra, Alyssa Nylander, et al. B cells populating the multiple sclerosis brain mature in the draining cervical lymph nodes. Science translational medicine, 6(248):248ra107–248ra107, 2014
