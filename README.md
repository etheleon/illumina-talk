#RNA Input Quality

* Run a RNA Chip on Bioanalyzer
* Run a formaldehyde 1% agarose gel, stain with eth bromide
* (Optional for TruSeq Small RNA) 

**QC**
* RNA integrity number aka RIN value
  * NOTE: the input quality is the #1 most impt factor in RNA-Seq!
  * RIN is not reliable for all RNA extractions. (normal cutoff = 8; but for pathology samples, rin cutoffs @ 2 is alright) 
  so how? RIN is not useful. if the beginning sample SUCKS. 
  use DV200 = % fragments > 200 bp 
  NOTE: yield is positively corr with DV200 value. so increase input to increase output yield. 

* 260/230 ratio Elution buffers (OD ratios)
NOTE: column based extraction will carry forward into next reaction (eg. you can use ethanol precipitation)

(Single Cell RNA seq KIT)[http://www.clontech.com/US/Products/cDNA_Synthesis_and_Library_Construction/Next_Gen_Sequencing_Kits/Single_cell_RNA_Seq_Kits_for_mRNA_seq/Single_Cell_RNA_Seq_v3]

#rRNA removal
use Capture (using the polyA tail to fish out the eukaryotic mRNA; bias to the 3' end)
use TruSeq :: probe based capture


RNA-seq coverage

1. mRNA 

||Type of analysis 	| reads required|
|-|-----------------------|---------------|
|mRNA|Differential expression | 10-20M reads |
|mRNA|alle specific expression | 50-100M reads| 
|total RNA| splice variation | 50-100M |
|total RNA| complete annotation | 100 -1Billion Reads| 
|total RNA| Transcript Based Assembly 50-200 M reads| 
|Small RNA | Differential expression 	|1M reads (animals ; plants require more) 	|
|Small RNA | Discovery 			| 10-20 M reads (for animals; plants require more) 	| 


Ribo-zero (high qulity RNA library requires 2X more reads - depending on application needs
Ribo-zero, FFPE libraries requires - 4X more reads - depending on applicaiton needs 



Data quality % > Q30

Data output % cluster pass filter and cluster density 
Equal sample representation in pool. 
Pooling is important

RNA expression 
95% of the differentially expressed may not be real. Hence we need to 
gold standard = qPCR

#RNA analyses
see paper by -> john c marioni christopher e mason

* correlation of fold change between arrays and RNAseq is similar to correlation between array platforms
* technical replicates are almost identical no need to run, 
* extra analysis prediction of alternative splicing, SNPs 
* low and high expressed genes do not match. (the dynamic range is better)


short reads distribution 
* poisson
* negative binomial 

the counts bet. diff samples will vary bet. samples. 

normalisation
  * FPKM
  * negative binomial
  * VST (variance stabilized transformation) 



short reads aligners
bowtie, novoalign, BWA, stampy, **StarSEQ**
starseq::not gd for quality assessment

data preprocessing (reads statistics, adap
* FGastx Toolkit
* MISO
* samtools
* Htseq


expression studies 
cufflinks package
RSEQtools
iDESeq

Alternative splicing
Clufflinks
Augustus

Commercial software
Partek
CLCBIO
