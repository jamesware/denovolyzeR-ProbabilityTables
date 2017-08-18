# denovolyzeR-ProbabilityTables

This is a repository of code and source data to generate *de novo* mutation probability tables as described in [Samocha *et al*][Samocha], and suitable for use by the [**denovolyzeR**][Ware] software (see also [denovolyzeR.org][denovolyzer], and hosted on CRAN)

**Overview**  

- start with a "synthetic" vcf that contains every possible protein-coding SNP  
- at each genomic position we extract the trinucleotide context (which defines mutability)  
- VCF is annotated with Ensemble VEP to generate consequences of each SNP  
- Join that to a table of trinucleotide mutation probabilities  
  An annotated synthetic vcf generated in this way is hosted [on the exac ftp][exacFtp]  

- Sum probabilities while grouping by gene & variant consequence  
  = "uncorrected" de novo mutation expectation  
- Apply sequence coverage connection (uses a separate file with % of bases covered at threshold for each gene, and multiple per gene probabilities by correction factor)  
- Apply longer-range mutability correction (human / macaque divergence - again a simple calculation applied to each gene)  




[Samocha]: http://www.nature.com/doifinder/10.1038/ng.3050
  "Samocha et al. Nature Genetics 2014"
[Ware]: http://onlinelibrary.wiley.com/doi/10.1002/0471142905.hg0725s87/abstract
	"Ware et al. Current Protocols in Human Genetics 2015"
[denovolyzer]: http://denovolyzeR.org
  "denovolyzeR.org"
[exacFtp]: ftp://ftp.broadinstitute.org/pub/ExAC_release/current/manuscript_data/all_possible_variants
  "exac ftp"
