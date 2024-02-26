# Genome_analysis_Unit_2
Material for Unit 2 of BIOL 3411: Principles and Methods of Genome Analysis at Northeastern University.

## Deliverable 2A
Work through through the material for ["Week 4 - What is a genomic variant?"](https://baylab.github.io/MarineGenomicsSemester/week-4--what-is-a-genetic-variant.html) , part of a course designed by Serena Caplins and Patrick Krug. Follow the instructions on the Deliverables 2A document, which has modifications specific to the Discovery Cluster. This exercise is an introduction to the various steps involves in analyzing NGS sequencing reads.

## Deliverable 2B
Complete the bowtie tutorial ["Lambda phage example"](https://bowtie-bio.sourceforge.net/bowtie2/manual.shtml#getting-started-with-bowtie-2-lambda-phage-example), documenting your progress with screenshots or saved terminal sessions.

## Deliverable 2C
Complete In_class_prep_Feb14. This exercise strengthens your skills in working with sequencing reads and prepares you to work with real data. Submit this deliverable as a pdf either on GitHub or in a folder on the Cluster.

## Deliverable 2D
Some of this exercise overlaps with Deliverable 2C, but this is meant to be done as a separate exercise. Submit this deliverable by including each of these components plus a file with their specific locations:
- raw data for each of the three datasets
- processed data (such as unzipped versions)
- QC reports
- saved sessions or screenshots showing the commands you used and their output while performing the exercise below
- list of tools: What are all the programs we have used so far? Where are they located (such as, in the available modules or as a separate environment in the shared folder)?
- narrative description of the operations you performed, as if you were explaining the project to a potential co-op hirer.

### Exercise
Three data sets consisting of NGS sequencing reads:
-	lambda phage from bowtie tutorial
-	Ppar reads from Marine Genomics course
-	Day lab reads

*****************************************************************************
Perform this first set of operations for all three datasets.
*****************************************************************************
Prepare a separate directory for each project, with subdirectories as needed.

First let’s describe the data we have. For each set of fastq files, describe:
1. How many reads are in each file 
2. The length of the reads and if they are single or paired-end
3. The overall quality of the reads and anything to be concerned about
4. Whether they appear to have adapter sequences that need to be trimmed

Collect quality control data on the reads, in the form of an .html file produced by fastqc.

If the sequences of a project need trimming, perform this step as described in the Marine Genomics tutorial, using cutadapt.

*****************************************************************************
For now, leave the Day data and perform the rest of the operations only on the lambda phage and Ppar (sea cucumber) data.
*****************************************************************************
Index the genome for each species using bowtie. 

Map the reads to the genome using bowtie. (How is the command used in the Marine Genomics tutorial different from that used in the bowtie tutorial?)

Convert the files containing mapped reads from sam to bam files using samtools.

There are two programs for determining variants (positions where the read sequences differ from the reference genome) that we were introduced to: bcftools and angsd. Use each of these to call variants for the lambda phage and sea cuke data, and compare the results.

Note that the bcftools protocol requires input files to be in a “sorted.bam” format, whereas angsd takes bam files as input.
