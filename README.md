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

2. Install Qiime2
```
conda create -n qiime2-2017.8 --file https://data.qiime2.org/distro/core/qiime2-2017.8-conda-osx-64.txt
```

## Running Software

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
