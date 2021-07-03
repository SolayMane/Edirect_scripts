# Edirect_scripts
## These lines of Scripts could help you to gather ressources from genbank using edirect tools

### 1) Interact with nuclotide database to search the sequence id "LT906355", the result will be piped to efectch commad to get the output in gpc format
````bash
esearch -db nuccore -query "LT906355" | efetch -format gpc | xtract -insd source organism strain
LT906355.1      Fusarium oxysporum MN25 NRRL54003
````
# How to retrive big genomes (plants) from  Genbank in one line

# Download all ericales genomes from ncbi
# We will look in docsum files which pattern to extract
````bash
esearch -db assembly -query "argania spinosa[orgn] AND latest[filter]" | efetch -format docsum

<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE DocumentSummarySet PUBLIC "-//NLM//DTD esummary assembly 20210618//EN" "https://eutils.ncbi.nlm.nih.gov/eutils/dtd/20210618/esummary_assembly.dtd">

<DocumentSummarySet status="OK">
<DocumentSummary>
<Id>1772241</Id>
        <RsUid></RsUid>
        <GbUid>6716858</GbUid>
        <AssemblyAccession>GCA_003260245.1</AssemblyAccession>
        <LastMajorReleaseAccession>GCA_003260245.1</LastMajorReleaseAccession>
        <LatestAccession></LatestAccession>
        <ChainId>3260245</ChainId>
        <AssemblyName>arg_spin_01</AssemblyName>
        <UCSCName></UCSCName>
        <EnsemblName></EnsemblName>
        <Taxid>85884</Taxid>
        <Organism>Argania spinosa (eudicots)</Organism>
        <SpeciesTaxid>85884</SpeciesTaxid>
        <SpeciesName>Argania spinosa</SpeciesName>
        <AssemblyType>haploid</AssemblyType>
        <AssemblyClass>haploid</AssemblyClass>
        <AssemblyStatus>Scaffold</AssemblyStatus>
        <AssemblyStatusSort>5</AssemblyStatusSort>
        <WGS>QLOD01</WGS>
        <GB_BioProjects>
                <Bioproj>
                        <BioprojectAccn>PRJNA294096</BioprojectAccn>
                        <BioprojectId>294096</BioprojectId>
                </Bioproj>
        </GB_BioProjects>
        <GB_Projects>
        </GB_Projects>
        <RS_BioProjects>
        </RS_BioProjects>
        <RS_Projects>
        </RS_Projects>
        <BioSampleAccn>SAMN04014715</BioSampleAccn>
        <BioSampleId>4014715</BioSampleId>
        <Biosource>
                <InfraspeciesList>
                </InfraspeciesList>
                <Sex></Sex>
                <Isolate>AM-2015</Isolate>
        </Biosource>
        <Coverage>120</Coverage>
        <PartialGenomeRepresentation>false</PartialGenomeRepresentation>
        <Primary>6716828</Primary>
        <AssemblyDescription></AssemblyDescription>
        <ReleaseLevel>Major</ReleaseLevel>
        <ReleaseType>Major</ReleaseType>
        <AsmReleaseDate_GenBank>2018/06/22 00:00</AsmReleaseDate_GenBank>
        <AsmReleaseDate_RefSeq>1/01/01 00:00</AsmReleaseDate_RefSeq>
        <SeqReleaseDate>2018/06/22 00:00</SeqReleaseDate>
        <AsmUpdateDate>2019/08/16 00:00</AsmUpdateDate>
        <SubmissionDate>2018/06/22 00:00</SubmissionDate>
        <LastUpdateDate>2019/08/16 00:00</LastUpdateDate>
        <SubmitterOrganization>IRIDIAN GENOMES</SubmitterOrganization>
        <RefSeq_category>representative genome</RefSeq_category>
        <AnomalousList>
        </AnomalousList>
        <ExclFromRefSeq>
        </ExclFromRefSeq>
        <PropertyList>
                <string>full-genome-representation</string>
                <string>latest</string>
                <string>latest_genbank</string>
                <string>representative</string>
                <string>wgs</string>
        </PropertyList>
        <FromType></FromType>
        <Synonym>
                <Genbank>GCA_003260245.1</Genbank>
                <RefSeq></RefSeq>
                <Similarity></Similarity>
        </Synonym>
        <ContigN50>43178</ContigN50>
        <ScaffoldN50>49916</ScaffoldN50>
        <FtpPath_GenBank>ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/003/260/245/GCA_003260245.1_arg_spin_01</FtpPath_GenBank>
        <FtpPath_RefSeq></FtpPath_RefSeq>
        <FtpPath_Assembly_rpt>ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/003/260/245/GCA_003260245.1_arg_spin_01/GCA_003260245.1_arg_spin_01_assembly_report.txt</FtpPath_Assembly_rpt>
        <FtpPath_Stats_rpt>ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/003/260/245/GCA_003260245.1_arg_spin_01/GCA_003260245.1_arg_spin_01_assembly_stats.txt</FtpPath_Stats_rpt>
        <FtpPath_Regions_rpt></FtpPath_Regions_rpt>
        <Busco>
                <RefSeqAnnotationRelease></RefSeqAnnotationRelease>
                <BuscoLineage></BuscoLineage>
                <BuscoVer></BuscoVer>
                <Complete></Complete>
                <SingleCopy></SingleCopy>
                <Duplicated></Duplicated>
                <Fragmented></Fragmented>
                <Missing></Missing>
                <TotalCount>0</TotalCount>
        </Busco>
        <SortOrder>2C5X90889999568210032602459800</SortOrder>
        <Meta><Stats> <Stat category="alt_loci_count" sequence_tag="all">0</Stat> <Stat category="chromosome_count" sequence_tag="all">0</Stat> <Stat category="contig_count" sequence_tag="all">78992</Stat> <Stat category="contig_l50" sequence_tag="all">4281</Stat> <Stat category="contig_n50" sequence_tag="all">43178</Stat> <Stat category="non_chromosome_replicon_count" sequence_tag="all">0</Stat> <Stat category="replicon_count" sequence_tag="all">0</Stat> <Stat category="scaffold_count" sequence_tag="all">75327</Stat> <Stat category="scaffold_count" sequence_tag="placed">0</Stat> <Stat category="scaffold_count" sequence_tag="unlocalized">0</Stat> <Stat category="scaffold_count" sequence_tag="unplaced">0</Stat> <Stat category="scaffold_l50" sequence_tag="all">3696</Stat> <Stat category="scaffold_n50" sequence_tag="all">49916</Stat> <Stat category="total_length" sequence_tag="all">670096797</Stat> <Stat category="ungapped_length" sequence_tag="all">667113929</Stat> </Stats> <FtpSites>   <FtpPath type="Assembly_rpt">ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/003/260/245/GCA_003260245.1_arg_spin_01/GCA_003260245.1_arg_spin_01_assembly_report.txt</FtpPath>   <FtpPath type="GenBank">ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/003/260/245/GCA_003260245.1_arg_spin_01</FtpPath>   <FtpPath type="Stats_rpt">ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/003/260/245/GCA_003260245.1_arg_spin_01/GCA_003260245.1_arg_spin_01_assembly_stats.txt</FtpPath> </FtpSites> <assembly-level>8</assembly-level> <assembly-status>Scaffold</assembly-status> <representative-status>representative genome</representative-status> <submitter-organization>IRIDIAN GENOMES</submitter-organization></Meta>
</DocumentSummary>
</DocumentSummarySet>

# now we will target ftppath_genbank element in docusum
# you can replace ericales by the name of your species/genus de download thier genomes
wget `esearch -db assembly -query "ericales[orgn] AND latest[filter]" | efetch -format docsum | xtract -pattern DocumentSummary -element FtpPath_GenBank | awk -F"/" '{print $0"/"$NF"_genomic.fna.gz"}'`
