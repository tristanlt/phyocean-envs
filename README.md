<h1 align="center">PhyOcean environments</h1>

µMamba/Anaconda environments for ocean physics. PhyOceans envs could be considered as "know good sets" of software and libraries useful for working at LOPS Laboratory (but it's not mandatory). These environments are useful to start with data processing instead of fighting in dependencies hell.

But what is a environment ? An environment is a set of tools installed inside a folder instead of system wide. Classically, environments are useful when you don't have administration rights (HPC center, workstation locked by strange sysadmin) or when you have to switch between versions of the same modules.

Environments could be preinstalled by system administrators or built by user on home directory (local or network).

Why used PhyOcean instead of choosing your products yourself
 * Dehydrated software (just add water)
 * Commons envs to share scripts with your colleagues
 * Not only for Python
 * 🔜 Tested with our scripts

Two environments are fixed per year (May and November), *fromveur* environment haven't fixed versions, so use it with caution.

## Available environments (stable)

--------
### PhyOcean 2021.05
* Platform(s) : 🐧 🍏
* Codename: `phyocean-2021.05`
* Download : [phyocean-2021.05.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/phyocean-2021.05.yaml)

<table>
<tr>
<th> Category </th>
<th> Items </th>
</tr>
</tr>
<td> 🚨 </td>
<td> Python 3.8, Cuda 11, Dask 2021.4, Numpy 1.20, Pandas 4.5, Tensorflow 2.4, Scikit 0.24, xarray 0.17 </td>
</tr>
</tr>
<td> Python </td>
<td> Cerbere, gsw 3.4, gpxpy, matplotlib, mpi4py, rasterio, Bokeh 2.3, Cython 0.29, netcdf4 1.5</td>
</tr>
</tr>
<td> Python (data) </td>
<td> Zarr 2.8, intake 0.6, s3fs, cdsapi, Cerbere, Google Cloud Storage, ESGF Pyclient</td>
</tr>
</tr>
<td> Development </td>
<td> JupyterLab 3, Spyder, nodeJS 15, ncview, NCO Tools </td>
</tr>
</table>

--------
### PhyOcean 2020.11
* Platform(s) : 🐧 🍏
* Codename: `phyocean-2020.11`
* Download : [phyocean-2020.11.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/phyocean-2021.10.yaml)

<table>
<tr>
<th> Category </th>
<th> Items </th>
</tr>
</tr>
<td> 🚨 </td>
<td> Python 3.6, Cuda 10, Dask 2021.1, Numpy 1.18, Pandas 1.1, Tensorflow 1.10, Scikit 0.24, xarray 0.16 </td>
</tr>
</tr>
<td> Python </td>
<td> gsw 3.4, gpxpy, matplotlib, mpi4py, rasterio, Bokeh 1.4, Cython 0.29, netcdf4 1.5</td>
</tr>
</tr>
<td> Python (data) </td>
<td> Zarr 2, intake, s3fs, cdsapi, Google Cloud Storage, ESGF Pyclient</td>
</tr>
</tr>
<td> Development </td>
<td> JupyterLab 2.0, nodeJS 13</td>
</tr>
</table>

---------

### PhyOcean "Fromveur"
* Platform(s) : 🐧 🍏
* Codename: `phyocean-fromveur`
* Download : [phyocean-fromveur.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/phyocean-fromveur.yaml)

🚨 Software versions are not pinned. Software/modules could be added or removed... Please read yaml file for details.

## Using PhyOcean envs at LOPS

JupyterHub users, PhyOcean are registered as kernel on JupyterHub LOPS services ([see LOPS internal docs](https://collab.umr-lops.fr/fr/systeme/moyens-de-calcul/kiosque-jupyter-hub))

LOPS-IUEM users, these environments are available with `module` on workstation or computing facilities.
```
module load envs/phyocean-2021.05
```

## Using PhyOcean envs on your computer

### Conda/Anaconda

First, install Anaconda, read install instructions from [Anaconda documentation](https://docs.anaconda.com/anaconda/install/).

Download chosen environment file. Latest stable is [phyocean-2021.05.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/phyocean-2021.05.yaml) or unfixed [phyocean-fromveur.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/phyocean-fromveur.yaml).

```
conda env create -f ~/Downloads/phyocean-2021.05.yaml
```
Next, activate env with
```
conda activate phyocean-2021.05
```

### MicroMamba

⚠️ bash & zsh shell on Linux & OS X only

microMamba is an open-source implementation of Conda, it aims to be lighter and faster than Conda. microMamba is fully compatible with Conda package, repositories (conda-forge) and environment files.

First, install microMamba, read install instructions from [Mamba documentation](https://mamba.readthedocs.io/en/latest/micromamba.html).

```
micromamba create -f phyocean-2021.05.yaml
```
Next, activate env with
```
micromamba activate phyocean-2021.05
```

