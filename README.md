# Copernicus Marine Toolbox Data Access

## Overview

This repository provides tutorials and example workflows for downloading and accessing datasets from the Copernicus Marine Service using its API. It includes Jupyter notebooks demonstrating various download methods, data processing, and visualization techniques for marine data.

## Setup

### 1. Conda environment setup

A dedicated Conda environment should be created to install the Copernicus Marine Service toolbox and the associated scientific Python libraries. This environment is intended for data download, preliminary inspection, and basic visualization of the retrieved datasets.

The environment can then be created using `mamba` for parallel downloading and faster installation:

```bash
mamba env create -f environment.yml
```

---

### 2. Environment activation and Jupyter configuration

After installation, the environment should be activated and registered as a Jupyter kernel to ensure that all subsequent notebook-based workflows use the correct Python environment.

Activate the environment:

```bash
conda activate cmems
```

Then, install the kernel for Jupyter:

```bash
python -m ipykernel install --user --name cmems --display-name "Copernicus Marine"
```

---

### 3. Copernicus Marine authentication

To enable authenticated access to the Copernicus Marine Service, user credentials should be configured once at the system level. This can be achieved by executing the login command in a terminal session, which generates a local credential file. This file allows repeated data access without re-entering authentication details for each download request.

```bash
conda activate cmems
copernicusmarine login
```

Please follow [`Copernicus_Marine_Toolbox.ipynb`](Copernicus_Marine_Toolbox.ipynb) for detailed descriptions of the available download methods.
The [`PS113_PFT_and_SST_Data.ipynb`](PS113_PFT_and_SST_Data.ipynb) notebook shows how to download the dataset covering the RV *Polarstern* PS113 expedition region.

