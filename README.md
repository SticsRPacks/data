# Example data for SticsRPacks

## Introduction
This repository contains example data used in `SticsRPacks`.

## Download

### Non-coders
If you don't have a GIT client installed, or if you don't even know what GIT is, you can download all the template files at once using this [link](https://github.com/SticsRPacks/data/archive/master.zip).

### Experienced users
To clone the repository, use this command:
```
git clone https://github.com/SticsRPacks/data.git
```
### From R

All steps are made using R directly in this example.

1. The first step is to download (or clone) this repository to get the data. For this example, we will download the repository into a temporary directory created from R.

    * If you have `GIT` installed on your computer:
```r
# install.packages("git2r")
data_dir= normalizePath(tempdir(), winslash = "/", mustWork = FALSE)
git2r::clone("https://github.com/SticsRPacks/data.git",data_dir)
```

    * or else, downloading the `ZIP` archive:
```r
data_dir= normalizePath(tempdir(), winslash = "/", mustWork = FALSE)
data_dir_zip= normalizePath(file.path(data_dir,"master.zip"), winslash = "/", mustWork = FALSE)
download.file("https://github.com/SticsRPacks/data/archive/master.zip", data_dir_zip)
unzip(data_dir_zip, exdir = data_dir)
unlink(data_dir_zip)
data_dir= normalizePath(list.dirs(data_dir)[2])
```

And now the data is available at the `data_dir` path for further use.


## Data

Some details about the data.

### Study Case 1

A simple parameter estimation with a single situation and a single observed variable. This data comes from a maize crop experiment (see description in Wallach et al., 2011).
