# PipeAIRR


PipeAIRR contains [DolphinNext](https://dolphinnext.readthedocs.io/en/latest/index.html#) pipelines for adaptive immune receptore repertoire sequencing (AIRR-seq) processing.

We have devided the pipelines into two main sections:
1. Pre-processing
2. Downstream analysis

##  Repository layout

In each section directory you can find each of the pipelines directories containing the dolphinnext pipeline (XX.dn) as well as the configurations and the nextflow script (XX.nf)

## Pre-processing

In this section you can find pipelines to process the sequencer output files, meaning from 'raw reads' into an aligner ready fasta file.

The pipeplines were build based on the [immcantation](https://immcantation.readthedocs.io/en/stable/) framework and spesificly the [pRESTO](https://presto.readthedocs.io/) tool suite.

### Available pipelines:


- [pipline1](https://github.com/PipeAIRR/pipeline1) - [Stern2014](https://presto.readthedocs.io/en/stable/workflows/Stern2014_Workflow.html) - UMI Barcoded Illumina MiSeq 2x250 BCR mRNA
- [pipline2](https://github.com/PipeAIRR/pipeline2) - [Greiff2014](https://presto.readthedocs.io/en/stable/workflows/Greiff2014_Workflow.html) - Illumina MiSeq 2x250 BCR mRNA
- [pipline3](https://github.com/PipeAIRR/pipeline3) - [VanderHeiden2017](https://presto.readthedocs.io/en/stable/workflows/VanderHeiden2017_Workflow.html) - UMI Barcoded Illumina MiSeq 325+275 paired-end 5’RACE BCR mRNA
- [pipline4](https://github.com/PipeAIRR/pipeline4) - [Galson2020](https://www.frontiersin.org/articles/10.3389/fimmu.2020.605170/full) - UMI Barcoded Illumina MiSeq 2x300 BCR mRNA with FR1 primers
- [pipline5](https://github.com/PipeAIRR/pipeline5) - [Yaari1](https://bitbucket.org/yaarilab/processpipeline/src/master/pre_process/Pipeline_P1.sh) - 5'RACE UMI barcoded Illumina Miseq 2x300 pair-end
- [pipline6](https://github.com/PipeAIRR/pipeline6) - [Yaari2](https://bitbucket.org/yaarilab/processpipeline/src/master/pre_process/Pipeline_P11.sh) - 5'RACE M1S and Z tags to sample pair-end reads

## Downstream analysis

In this section you can find pipelines to analyze processed reads and infer genotype and haplotype.

The pipeplines were build based on the [Yaari lab framework](https://hub.docker.com/repository/docker/peresay/suite), that contains tools from:
- [immcantaton](https://immcantation.readthedocs.io/en/stable/)
- [VDJbase](vdjbase.org)
- [TIgGER](https://tigger.readthedocs.io/en/stable/)
- [RAbHIT](https://yaarilab.bitbucket.io/RAbHIT/)
- [PIgLET](https://yaarilab.github.io/IGHV_reference_book/piglet_package.html)

### Available pipelines:
- [ASC2022](https://yaarilab.github.io/IGHV_reference_book/allele_based_genotype.html) - IGH BCR repertoires analysis with IgBLAST sequence alignment, novel allele inference by TIgGER, and genotype inference by PIgLET.
