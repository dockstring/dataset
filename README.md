# Dockstring Dataset

This repo contains sample code to help download and extract the dockstring dataset.

## Downloading the dataset

The following shell commands can be used to download the whole dataset:

```bash
# Download whole dataset into a data directory and unzip it
mkdir -p data
wget https://figshare.com/ndownloader/articles/16511577/versions/1 -O data/data.zip
unzip data/data.zip -d data

# Decompress the poses with `unxz`
# The `-k` option keeps the original compressed file
for fname in data/*.sdf.xz ; do unxz -k $fname ; done
```

## Tutorials

The following tutorials may be useful:

1. [Loading the dataset with pandas](0_load_dataset.ipynb)
2. [Loading and visualizing the docking poses with rdkit](1_visualize_dataset_pose.ipynb)
