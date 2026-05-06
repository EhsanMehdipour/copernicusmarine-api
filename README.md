# Copernicus Marine Toolbox Data Access
This repository explains the methods to download datasets from copernicus marine service API functionality.

# Setup

## 1. Conda environment setup

A dedicated Conda environment should be created to install the Copernicus Marine Service toolbox and the associated scientific Python libraries. This environment is intended for data download, preliminary inspection, and basic visualization of the retrieved datasets.

The environment can then be created using `mamba` for parallel downloading and faster installation:

```bash
mamba env create -f environment.yml
```

---

## 2. Environment activation and Jupyter configuration

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

## 3. Copernicus Marine authentication

To enable authenticated access to the Copernicus Marine Service, user credentials should be configured once at the system level. This can be achieved by executing the login command in a terminal session, which generates a local credential file. This file allows repeated data access without re-entering authentication details for each download request.

```bash
conda activate cmems
copernicusmarine login
```

Please follow the `Copernicus_Marine_Toolbox.ipynb` for the descriptions of the several downloading methods.