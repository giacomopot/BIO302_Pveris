# BIO302 - Nanopore

## File location
As a first step, create a new history and import the data:
* In the Galaxy main page, click on the "+" symbol next to "History" (top right of the screen).
* Rename the History as `BIO302 <name of your species>`.

All the data needed for your project are available in [this Galaxy history](https://usegalaxy.eu/u/giacomopot/h/bio302-2024-files). Click `Import history` on the tope left of the screen. Depending on which species you will be working on, keep only the files relevant to your project:
* _Primula edelbergii_ (Ped):
  * `Pedelbergii.ont.fastq.gz`: Nanopore reads
  * `Pedelbergii.hic.R1.fastq.gz`, `Pedelbergii.hic.R2.fastq.gz`: Hi-C reads
* _Primula veris_ (Pve):
  * `Pveris.ont.fastq.gz`: Nanopore reads
  * `Pveris.hic.R1.fastq.gz`, `Pveris.hic.R2.fastq.gz`: Hi-C reads 

## Software used
This is a list of the main software used in these labs. The links will take you to general tutorials for each software.
Here are described the main steps 
### Input data QC and genome profiling
Check the distribution of length and quality in your long-read data set. Perform a genome profiling through k-mer analysis to estimate genome size and heterozygosity (i.e. proportion of heterozygous sites across the genome).
* QC on long reads ([Nanoplot](https://training.galaxyproject.org/topics/assembly/tutorials/chloroplast-assembly/tutorial.html#check-read-quality))
* Genome profiling with k-mer analysis ([Meryl + GenomeScope](https://training.galaxyproject.org/topics/assembly/tutorials/vgp_genome_assembly/tutorial.html#genome-profile-analysis))

### Genome assembly and first QC
Assemble a draft genome assembly using long reads. Obtain stats about the completeness and contiguity of the draft assembly.
* Genome assembly ([Shasta](https://usegalaxy.eu/root?tool_id=toolshed.g2.bx.psu.edu/repos/iuc/shasta/shasta/0.6.0+galaxy0))
* Draft assembly QC ([BUSCO and Quast](https://training.galaxyproject.org/topics/assembly/tutorials/assembly-quality-control/tutorial.html#k-mer-based-assembly-evaluation-with-merqury))

### Assembly scaffolding and second QC
Use Hi-C reads to scaffold the draft assembly. Obtain stats about the completeness and contiguity of the scaffolded (i.e. final) assembly.
* Hi-C scaffolding ([YaHS](https://training.galaxyproject.org/topics/assembly/tutorials/vgp_genome_assembly/tutorial.html#hi-c-scaffolding))
* Scaffolded assembly QC ([BUSCO and Quast](https://training.galaxyproject.org/topics/assembly/tutorials/assembly-quality-control/tutorial.html#k-mer-based-assembly-evaluation-with-merqury))

### Annotate the genome
Identify repetitive regions and genes in the final genome assembly.
* Repeat annotation ([EDTA](https://usegalaxy.eu/?tool_id=toolshed.g2.bx.psu.edu%2Frepos%2Fbgruening%2Fedta%2Fedta%2F2.1.0%2Bgalaxy0&version=latest))
* Gene annotation ([Maker](https://training.galaxyproject.org/topics/genome-annotation/tutorials/annotation-with-maker/tutorial.html))
