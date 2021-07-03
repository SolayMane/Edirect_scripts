# Edirect_scripts
## These lines of Scripts could help you to gather ressources from genbank using edirect tools

### 1) Interact with nuclotide database to search the sequence id "LT906355", the result will be piped to efectch commad to get the output in gpc format
````bash
esearch -db nuccore -query "LT906355" | efetch -format gpc | xtract -insd source organism strain
LT906355.1      Fusarium oxysporum MN25 NRRL54003



# download all ericla genomes from ncbi
wget `esearch -db assembly -query "ericales[orgn] AND latest[filter]" | efetch -format docsum | xtract -pattern DocumentSummary -element FtpPath_GenBank | awk -F"/" '{print $0"/"$NF"_genomic.fna.gz"}'`
