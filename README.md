# bacteria_genome_pull
Download latest bacterial sequencing assembly files from NCBI database (RefSeq or Genbank)

To access help menu:

`python bacteria_genome_pull.py` or `python bacteria_genome_pull.py -h`

###Basic Usage:
`python bacteria_genome_pull.py -b Klebsiella_pneumoniae`
  
This will download all latest assembly sequencing files in *fna* format for Klebsiella pneumoniae from **refseq**. All files will be downloaded to current directory.


###Change NCBI database:
`python bacteria_genome_pull.py -d genbank -b Klebsiella_pneumoniae`

If no -d argument is given, will default to **refseq**


###Change file type:
`python bacteria_genome_pull.py -t gff -b Klebsiella_pneumoniae`

This will download the *gff* file for all Klbesiella pneumoniae genomes in **refseq**

If no -t argument is given, will default to *fna*


###Which genomes are available:
`python bacteria_genome_pull.py -g refseq`

This will provide a list of all available bacterial genomes in **refseq**


###Specify output directory:
`python bacteria_genome_pull.py -b Klebsiella_pneumoniae -o path/to/foo`

Will output all *fna* files to foo directory.

This will create foo directory if it does not exist.


###Argument Options:
|Argument      |Explanation     | Option(s)|
|--------------|-----------|------------|
|-b (required) |bacterium  |name of bacterium|
|-t (optional) |file type  |fna (default)|
|              |           |gbb  |
|              |           |genbank   |
|              |           |feature_table  |
|-d (optional) |database   |refseq (default)|
|              |           |genbank   |
|-g (optional) |available genomes |refseq (default) |
|              |                  |genbank  |
|-o (optional) |output directory |. (defualt) |


#Examples

####Download all refseq bacterial genomes (in fna format)
`python bacteria_genome_pull.py -b *`

####Download all Klebsiella genbank files from refseq
`python bacteria_genome_pull.py -t genbank -b Klebsiella*`

####Download all Klebsiella pneumoniae gff files from genbank and store in foo directory
`python bacteria_genome.py -t gff -d genbank -o directory -b Klebsiella_pneumoniae`






