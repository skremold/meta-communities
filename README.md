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

2. Install Qiime1
```
conda create -n qiime1 python=2.7 qiime matplotlib=1.4.3 mock nose -c bioconda
```

## Running Software

```
source activate qiime1
```



