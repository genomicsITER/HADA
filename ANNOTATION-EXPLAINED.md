## Different parameters can be annotated with HADA, explained below:

* **CHR**: chromosome.
* **POS (hg19)**: genomic coordinates of the variant according to `GRCh37/hg19` build.
* **REF**: reference allele in `GRCh37/hg19`.
* **ALT**: alternative allele observed in the sample.
* **GENE**: corresponding HUGO name of the gene contain of the variant.
* **EXON**: exon where the variant is located.
* **HGVS CODING**: indication of the change according to HGVS nomenclature, used to report and exchange information regarding variants found in DNA, RNA and protein sequences and serves as an international standard.
* **AMINOACID CHANGE**: The notation defined by the Human Genome Variation Society (HGVS), based on the position of the variant in the protein.
* **FUNCTION**: Gene function in human genome.
* **ACMG CLASSIFICATION**: pathogenicity classification build on-the-fly according to ACMG guidelines.
* **CLINVAR CLINICAL SIGNIFICANCE**: pathogenicity classification obtained from ClinVar.
* **INTERVAR CLASSIFICATION**: pathogenicity classification obtained from InterVar.
* **EFFECT**: coding effect of the indicated variant.
* **VARSOME LINK**: link to VarSome tool, provided with graphical representation of the variant location.
* **REFERENCE SNP CLUSTER ID**: rs ID for each variation (when it is available) obtained from avsnp150 database and scientific literature review.
* **NOTES**: HAEdb ID and pathogenicity classification and notes (HAE type, mutation effect in the protein, associated diseases, etc).
* **CITE**: reference citation where the mutation is detected. It is ordinated by chronogram.
* **DATABASE**: indication about where the mutation was detected and analyzed.
* **FUNC REF GENE**: indication about the nature of the variant.

---

### ExAC:
* **ExAC_ALL**: Allele frequency in total ExAC samples
* **EXAC_AFR**: Allele frequency in African/African American ExAC samples
* **EXAC_AMR**: Allele frequency in Latino ExAC samples
* **EXAC_EAS**: Allele frequency in East Asian ExAC samples
* **EXAC_FIN**: Allele frequency in Finnish ExAC samples
* **EXAC_NFE**: Allele frequency in Non-Finnish European ExAC samples
* **EXAC_SAS**: Allele frequency in South Asian ExAC samples
* **EXAC_OTH**: Allele frequency in Other ExAC samples

---

### gnomAD:
* **gnomAD_exome_ALL**: Allele frequency in total gnomAD samples
* **gnomAD_exome_AFR**: Allele frequency in African/African American gnomAD samples
* **gnomAD_exome_AMR**: Allele frequency in Admixed American gnomAD samples
* **gnomAD_exome_ASJ**: Allele frequency in Ashkenazi Jewish gnomAD samples
* **gnomAD_exome_EAS**: Allele frequency in East Asian gnomAD samples
* **gnomAD_exome_FIN**: Allele frequency in Finnish gnomAD samples
* **gnomAD_exome_NFE**: Allele frequency in Non-Finnish European gnomAD samples
* **gnomAD_exome_SAS**: Allele frequency in South Asian gnomAD samples
* **gnomAD_exome_OTH**: Allele frequency in Other gnomAD samples

---

### SIFT:
* **SIFT_SCORE**: Scores range from 0 to 1. The smaller the score the more likely the SNP has damaging effect.
* **SIFT_CONVERTED_RANKSCORE**: SIFT scores were first converted to `SIFTnew=1-SIFT`, then ranked among all new SIFTnew scores in dbNSFP. The rankscore is the ratio of the rank the SIFTnew score over the total number of SIFTnew scores in dbNSFP. If there are multiple scores, only the most damaging (largest) rankscore is presented. The rankscores range from `0.02654` to `0.87932`.
* **SIFT_PRED**: If SIFT score is smaller than `0.05` (`rankscore>0.55`) the corresponding NS is predicted as *D(amaging)*; otherwise it is predicted as *T(olerated)*.

---

### Polyphen2:
* **POLYPHEN2_HDIV_SCORE**: Polyphen2 score based on HumDiv, i.e. hdiv_prob. The score ranges from 0 to 1. 
* **Polyphen2_HDIV_rankscore**: Polyphen2 HDIV scores were first ranked among all HDIV scores in dbNSFP. The rankscore is the ratio of the rank the score over the total number the scores in dbNSFP. If there are multiple scores, only the most damaging (largest) of rankscore is presented. The scores range from `0.02656` to `0.89917`.
* **Polyphen2_HDIV_pred**: Polyphen2 prediction based on HumDiv, *D* (*probably damaging*, HDIV score in `[0.957,1]` or rankscore in `[0.52996,0.89917]`), *P* (*possibly damaging*, HDIV score in `[0.453,0.956]` or rankscore in `[0.34412,0.52842]`) and *B* (*benign*, HDIV score in `[0,0.452]` or rankscore in `[0.02656,0.34399]`). Score cutoff for binary classification is 0.5 for HDIV score or `0.35411` for rankscore, i.e. the prediction is neutral if the HDIV score is smaller than `0.5` (rankscore is smaller than `0.35411`), and *deleterious* if the HDIV score is larger than `0.5` (rankscore is larger than `0.35411`).

---

### MutationTaster:
* **MutationTaster_score**: MutationTaster p-value score (MTori), ranges from 0 to 1.
* **MutationTaster_converted_rankscore**: The scores were first converted: if the prediction is *A* or *D* `MTnew=MTori`; if the prediction is *N* or *P*, MTnew=1-MTori. Then MTnew scores were ranked among all MTnew scores in dbNSFP. The rankscore is the ratio of the rank of the score over the total number of MTnew scores in dbNSFP. The scores range from `0.09067` to `0.80722`.
* **MutationTaster_pred**: MutationTaster prediction, *A* (*disease_causing_automatic*), D (*disease_causing*), *N* (*polymorphism*) or *P* (*polymorphism_automatic*). The score cutoff between *D* and *N* is `0.5` for MTori and `0.31655` for the rankscore.

---

### Combined Annotation Dependent Depletion (CADD):
* **CADD_raw**: CADD raw score for funtional prediction of a SNP. The larger the score the more likely the SNP has damaging effect.
* **CADD_raw_rankscore**: CADD raw scores were ranked among all CADD raw scores in dbNSFP. The rankscore is the ratio of the rank of the score over the total number of CADD raw scores in dbNSFP
* **CADD_phred**: CADD phred-like score. This is phred-like rank score based on whole genome CADD raw scores. The larger the score the more likely the SNP has damaging effect. 

---

### Deep Neural Network (DANN):
* **DANN_score**: DANN is a functional prediction score retrained based on the training data of CADD using deep neural network. Scores range from 0 to 1. A larger number indicate a higher probability to be damaging.

* **DANN_rankscore**: DANN scores were ranked among all DANN scores in dbNSFP. The rankscore is the ratio of the rank of the score over the total number of DANN scores in dbNSFP.

---

### Likelihood Ratio Test (LRT):
* **LRT_score**: The likelihood ratio test (LRT) is a statistical test of the goodness-of-fit between two models. The original LRT two-sided p-value (LRTori), ranges from 0 to 1.
* **LRT_converted_rankscore**: LRTori scores were first converted as `LRTnew=1-LRTori*0.5 if Omega<1`, or `LRTnew=LRTori*0.5 if Omega>=1`. Then LRTnew scores were ranked among all LRTnew scores in dbNSFP. The rankscore is the ratio of the rank over the total number of the scores in dbNSFP. The scores range from `0.00166` to `0.85682`.
* **LRT_pred**: LRT prediction, *D(eleterious)*, *N(eutral)* or *U(nknown)*, which is not solely determined by the score.

---

### MetaSVM:
* **MetaSVM_score**: The support vector machine (SVM) is based on ensemble prediction score, which incorporated 10 scores (SIFT, PolyPhen-2 HDIV, PolyPhen-2 HVAR, GERP++, MutationTaster, Mutation Assessor, FATHMM, LRT, SiPhy, PhyloP) and the maximum frequency observed in the 1000 genomes populations. Larger value means the SNV is more likely to be damaging. Scores range from -2 to 3 in dbNSFP.
* **MetaSVM_rankscore**: MetaSVM scores were ranked among all MetaSVM scores in dbNSFP. The rankscore is the ratio of the rank of the score over the total number of MetaSVM scores in dbNSFP. The scores range from 0 to 1.
* **MetaSVM_pred**: Prediction of SVM based ensemble prediction score, classifying them as *T(olerated)* or D(amaging). The MetaSVM_score cutoff between *D* and *T* is 0. The MetaSVM_rankscore cutoff between *D* and *T* is `0.83357`.

---

### phastCons20:
* **phastCons20way_mammalian**: phastCons conservation score based on the multiple alignments of 20 mammalian genomes (including human). The larger the score, the more conserved the site. Scores range from 0 to 1.

* **phastCons20way_mammalian_rankscore**: phastCons20way_mammalian scores were ranked among all phastCons20way_mammalian scores in dbNSFP. The rankscore is the ratio of the rank of the score over the total number of phastCons20way_mammalian scores in dbNSFP.

---

### ClinPred: 
* **ClinPred** is an efficient tool for identifying disease-relevant nonsynonymous variants. It incorporates two machine learning algorithms that use existing pathogenicity scores and, notably, benefits from inclusion of normal population allele frequency from the gnomAD database as an input feature. ClinPred uses ClinVar – a rapidly growing database that allows selection of confidently annotated disease causing variants - as a training set. Variants with ClinPred scores over 0.5 can be considered as pathogenic.

