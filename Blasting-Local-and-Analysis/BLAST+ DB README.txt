#############################################################
README for ftp://ncbi.nlm.nih.gov/refseq/

Last updated: June 11, 2010

#############################################################

_________________________________________________________________________

       
       National Center for Biotechnology Information (NCBI)
             National Library of Medicine
             National Institutes of Health
             8600 Rockville Pike
             Bethesda, MD 20894, USA
             tel: (301) 496-2475
             fax: (301) 480-9241
             e-mail: info@ncbi.nlm.nih.gov
             
_________________________________________________________________________

=========================================================================
UPDATES TO THIS FTP SITE:

  July 2, 2003	
  RefSeq Release 1 is available by anonymous FTP 
  ftp://ftp.ncbi.nih.gov/refseq/release/


  August 16, 2005
  Added documentation of the 'wgs' directory
  Removed 'cumulative' directory and related documentation 
  as it was replaced by the RefSeq release.
  Modified documentation of the LocusLink directory
  to reflect the obsolete/archival status.

  April 27, 2007
  Added documentation of 'special_requests' directory
  
  October 3, 2007
  Added documentation of the uniprotkb directory

  October 12, 2007
  Added documentation about the /removed/ directory

  June 11, 2010
  Modified format for new report files in the /removed/ directory
  to remove space padding for 'replaced-by' accession entries.
  Removed references to the historical resource LocusLink.  

See the README file and the RefSeq Release notes for more 
information:
ftp://ftp.ncbi.nih.gov/refseq/release/README
ftp://ftp.ncbi.nih.gov/refseq/release/release-notes/

	
=========================================================================
The NCBI Reference Sequence project (RefSeq) provides reference sequence
standards for the naturally occurring molecules of the central dogma, from
chromosomes to mRNAs to proteins. RefSeq standards provide a foundation for the
functional annotation of the human genome. They provide a stable reference
point for mutation analysis, gene expression studies, and polymorphism
discovery.

Scope: Currently, RefSeq records are provided for the following molecule types:

  Molecule Type		Accession Prefix
  ----------------------------------------------
  protein		NP_; XP_; ZP_; AP_; YP_;
  rna			NM_; NR_; XM_; XR_
  genomic		NC_; NG_; NT_; NW_; NZ_; NS_; AC


Additional information is available from 
http://www.ncbi.nih.gov/RefSeq/ 

_________________________________________________________________________
The following directories are available from this RefSeq ftp site:

   daily
   B_taurus
   D_rerio
   H_sapiens
   LocusLink
   M_musculus
   release
   removed
   R_norvegicus
   special_requests
   uniprotkb
   wgs
   X_tropicalis

==========================================
release
==========================================
Regular RefSeq releases are made available in this directory area.
The directory is organized into several sub-directories:

Directory		Contents
---------------------------------
complete		sequence
fungi			sequence
invertebrate		sequence
microbial		sequence
mitochondrion		sequence
plant			sequence	
plasmid			sequence
plastid			sequence
protozoa		sequence
release-catalog		documentation; 
			  . accessions included in the release
			  . files installed (sequence data) for the release
                          . accessions removed since last release
                          .  organisms added and changed since the last release
release-notes		documentation; 
                            content, scope, organization, structure
release-statistics	documentation; 
                            statistics per sequence directory
vertebrate_mammalian	sequence	
vertebrate_other	sequence
viral			sequence
               

==========================================
daily
==========================================
The daily directory contains daily updates of non-WGS refseq gi's
since the RefSeq release. This directory is not cumulative. The
contents of the directory are removed following the installation of 
a new RefSeq release. Release-related updates to this directory may 
result in an small number of retained files that represent sequences
that were released during the time period that the RefSeq release 
was being processed.

 
File name format:
 
        rsnc.[MonthDay.YEAR].bna.gz     Nucleotide sequence, in ASN.1 binary format
        rsnc.[MonthDay.YEAR].faa.gz     Protein sequences, in FASTA format
        rsnc.[MonthDay.YEAR].fna.gz     Nucleotide sequences, in FASTA format
        rsnc.[MonthDay.YEAR].gbff.gz    GenBank flatfile view (nucleotides)
        rsnc.[MonthDay.YEAR].gpff.gz    GenPept flatfile view (proteins)


==========================================
removed
==========================================
The removed directory contains daily update reports of RefSeq
records that have been removed from the collection since the 
last RefSeq release. If no records have been removed, then no file
is supplied for that day.  The directory is not cumulative and
contents are removed following the installation of a new RefSeq
release.  

File name format:
     removed-records.mmdd.yyyy

Columns (tab delimited)
  accession
  version
  gi
  removal category --where category may be one of:
  	  	   temporarily suppressed
		   permanently suppressed
		   temporarily withdrawn
		   permanently withdrawn
		   replaced by {accession} - see Note1. 
  removal date     --yyyy.mm.dd

NOTE1: the report file format has been updated to removed padded spaces 
       for those accessions in replaced-by entries.

NOTE2: there is an additional category of removal, reported as 
dead proteins in the RefSeq release report of removed records,
that is not currently included in this daily report. 

See also: 
ftp://ftp.ncbi.nih.gov/refseq/release/release-catalog/README
documentation for: release#.removed-records

==========================================
wgs
==========================================
The wgs directory contains daily updates of WGS refseq gi's
since the RefSeq release. This directory is not cumulative.
The contents of this directory are removed following the installation 
of a new RefSeq release. Release-related updates to this directory may 
result in an small number of retained files that represent sequences
that were released during the time period that the RefSeq release 
was being processed.

 
File name format:
 
        rswgs.[WGS_project].bna.gz     Nucleotide sequence, in ASN.1 binary format
        rswgs.[WGS_project].faa.gz     Protein sequences, in FASTA format
        rswgs.[WGS_project].fna.gz     Nucleotide sequences, in FASTA format
        rswgs.[WGS_project].gbff.gz    GenBank flatfile view (nucleotides)
        rswgs.[WGS_project].gpff.gz    GenPept flatfile view (proteins)



==========================================
Organism specific subdirectories
==========================================
Select organism specific files are also provided so that
previously provided service is not discontinued. We do 
not plan to add additional organism-specific directories
at this time. 

Data is updated weekly in a cycle independent of the RefSeq release,
cumulative, and daily update processing and constitutes a
full release of transcript and protein data for the organism.

ftp://ftp.ncbi.nih.gov/refseq/B_taurus/mRNA_Prot/
ftp://ftp.ncbi.nih.gov/refseq/D_rerio/mRNA_Prot/
ftp://ftp.ncbi.nih.gov/refseq/H_sapiens/mRNA_Prot/
ftp://ftp.ncbi.nih.gov/refseq/M_musculus/mRNA_Prot/
ftp://ftp.ncbi.nih.gov/refseq/R_norvegicus/mRNA_Prot/
ftp://ftp.ncbi.nih.gov/refseq/X_tropicalis/mRNA_Prot/

The sequence data is available in the following
formats:

  organism.protein.faa.gz  	protein fasta, zipped
  organism.protein.gpff.gz 	genpept flat file, zipped
  organism.rna.fna.gz   	 nucleotide fasta, zipped
  organism.rna.gbff.gz  	 nucleotide flat file, zipped


		
==========================================
special_requests
==========================================
Additional reports are provided upon request. The reports
may be limited in scope in that they report data for a 
sub-set of the RefSeq collection. 

See the special_requests/README file for additional information.

==========================================
uniprotkb
==========================================

In collaboration with UniProtKB, corresponding RefSeq to UniProt
protein accession data are now reported. 

UniProt calculates corresponding accessions based on the following criteria:

a) Identical sequence and identical species (NCBI tax_id) 
--the majority of the corresponding pairs fall into this category

b) Common protein ID and identical tax_id where both RefSeq and UniProt records 
cite the same protein accession as one that was used to create the RefSeq or 
UniProt record.

c) Common protein ID and equivalent but non-identical tax_id where the common 
protein ID is as above, and tax_ids are converted from strain or sub-strain 
level to the species level (e.g., UniProt and RefSeq may differ in their 
decisions to represent a sequence as the species vs a specific strain but 
they are based on the same underlying GenBank data and are considered 
equivalent).

File: gene_refseq_uniprotkb_collab
----------------------------------
Column header line is the first line in the file.
Columns are tab-delimited with one accession pair per line
Accession values are not unique; a single accession from
one database may have multiple corresponding accessions from
the other database.

Column 1: RefSeq protein accession
Column 2: UniProt protein accession 

