# meta-communities

skremold data analysis


requires `data` to contain the following files containing sequence data:

* Hundley_2652B.fna
* Hundley_2652B.qual
* Purdy_1937B.fna
* Purdy_1937B.qual


# Setup
## Software dependencies

1. Miniconda: [install](https://conda.io/docs/user-guide/install/index.html)
```
# Name: Miniconda2
# Version: 4.3.21
# Packages: 26
# PLAT:  osx-64
# DESCR: 4.4.0-76-g36f8d5b
# BYTES:  22438628
# LINES: 400
# MD5:   58deb8188a4278584826f3c34e1061c7
```

2. Qiime1
Install:
```
conda create -n qiime1 python=2.7 qiime matplotlib=1.4.3 mock nose -c bioconda
```

Running:

```
 source activate qiime1

# -b 8   Number representing the length of the barcode
# -p     Disable primer usage when demultiplexing
# Minimum sequence length, in nucleotides [default: 200]
# Maximum sequence length, in nucleotides [default: 1000]
# Min average qual score allowed in read [default: 25]
# Maximum number of ambiguous bases [default: 6]
# Maximum length of homopolymer run [default: 6]
# Maximum number of primer mismatches [default: 0]
# Maximum number of errors in barcode [default: 1.5]
# Retain sequences which are Unassigned in the output sequence file[default: False]


FILE_ROOT=Hundley_2652B

FILE_ROOT=Purdy_1937B
OUT_ROOT=out/${FILE_ROOT}
SOURCE_FASTA=data/${FILE_ROOT}.fna
SPLIT_FASTA=${OUT_ROOT}/split_lib/seqs.fna
split_libraries.py -m ${FILE_ROOT}.txt -b 8 -p -f ${SOURCE_FASTA} -q data/${FILE_ROOT}.qual -o ${OUT_ROOT}/split_lib/

# -m, --otu_picking_method [default: uclust]
OTUS_OUTDIR=${OUT_ROOT}/uclust_picked_otus
pick_otus.py -i out/${FILE_ROOT}/split_lib/seqs.fna -o ${OTUS_OUTDIR}

OTUS_TXT=${OTUS_OUTDIR}/seqs_otus.txt
pick_rep_set.py -i ${OTUS_TXT} -f ${SPLIT_FASTA} -o ${OUT_ROOT}/rep_set.fna


```




for i in "one" "two"
do
   echo "$i"
   # or do whatever with individual element of the array
done
















## Qiime2


2. Install Qiime2
```
conda create -n qiime2-2017.8 --file https://data.qiime2.org/distro/core/qiime2-2017.8-conda-osx-64.txt
```

3. Run Qiime2

```
source activate qiime2-2017.8
source tab-qiime
```



### Citacions

Lists software packages followed by citacions

```
qiime info --citations > qiime_info_citations.txt
```


### Deactivate the Qiime environment

```
source deactivate
```
