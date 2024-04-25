**QC conclusions**
---

**Nature & Quality of the data**
* The total number of reads per sample is insufficient for conducting a thorough exploratory analysis of any type (max around 3300 reads).
* Duplication rate is slightly higher in certain samples (10-20%) but still under the normal percentage range for NGS.
* Average percentage of GC content is within normal range of 39-42%. This means that most of the reads have GC percentage range of 39-42% as can be seen in FastQC report on the distribution plot of GC percentages of the reads per sample. 
* Average base quality per each read position is quite poor peaking only at Phred score = 12. Ideally, it must be above 30 (meaning only 0.001% chance of falsely calling the base during sequencing).
* Most of the reads are ~500 base pairs long for each sample but some are as long as 3000-4000 base pairs and some are even longer.
* Overrepresented sequences constitute a huge chunk of all the reads, which need to be removed by trimming software such as Cutadapt. Otherwise, if they do not originate from biological variation, they can skew the read count distribution later in the downstream analysis.
* Illumina universal adapter seems to be enriched at the 3'-end of some reads in certain samples which is an indication of usage of Illumina method of sequencing.
* PolyA sequence enrichment could be a sign of any type of mRNA sequencing (could be bulk or single-cell). Other types of RNA occasionally also contain polyA tails so we might be detecting them too.

**Type of sequencing**
* In my opinion, data comes from long-read RNA sequencing performed by the Illumina sequencing technique. Samples contain reads of about 3-10kb in length, which can only be achieved by long-read sequencing.

