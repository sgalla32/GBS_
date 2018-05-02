# GBS_Pre-Process_Trimming

Shell scripts that trims GBS reads to 64bp using Skewer and interleaves the files using shuffleSequences.pl in Velvet. 

Before running these scripts, assure the following:
1. Fastq files have been demultiplexed (Programme: Axe).
2. Fastq files have been trimmed for cut-sites using batch-trim.pl (Requires: Trim Galore!)
3. Fastq files have already had chimeras verified using verify_chimeras.pl 

You need the programmes Skewer and Velvet to run these scripts. 

For Skewer, you only need to write:
skewer -L 64 -e -q 0 'Location/SampleID_Forward_Read.fastq' 'Location/SampleID_Reverse_Read.fastq' - o 'Location/SampleID_After_Skewer'.

For Velvet, you only need the shuffleSequences_fastq.pl perl script, which is usually located in /home/velvet/contrib/shuffleSequences_fasta/shuffleSequences_fastq.pl
