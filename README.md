# gmos-sample

Sample files to show different behaviour when identical files are used vs. removing a sequence as a query

## 1_same

Input:

* Identical files are used as both query and subject 

Result:

* Each query sequence is positive for mosaicism with itself across the whole sequence
* No other mosaic regions are output

## 2_removed_query

Input:

* `seq_72` is removed from `1_same/1_original.fasta` and used as query `2_removed_query/1_query_seq72.fasta`
* All remaining sequences from `1_same/1_original.fasta` are used as subject `2_removed_query/1_1_subject_noseq72.fasta` i.e. all sequences, except `seq_72` are included in the subject file

Result:

* Expected behaviour(?), if mosaicism is present
* Multiple hits positive for mosaicism is output, across multiple sequences
