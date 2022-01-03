# ITS-regions_engine_ONT

This is a 




conda create --name ITS_engine
conda activate ITS_engine

conda install -c bioconda minimap2
conda install -c bioconda NanoFilt

###Download database from UNITE: https://unite.ut.ee/repository.php

minimap2 -ax map-ont --sam-hit-only sh_refs_qiime_ver8_dynamic_10.05.2021.fasta TEST.fa.txt | sed '/^@/d' > aln_sanitized.txt

cut -f1,3 < aln_sanitized.txt > aln_sanitized_IDs.txt
 
