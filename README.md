<h1 align="center">PhyOcean environments</h1>

µMamba/Anaconda environments for ocean physics. PhyOceans envs could be considered as "know good sets" of software and libraries useful for working at LOPS Laboratory (but it's not mandatory). These environments are useful to start with data processing instead of fighting in dependencies hell.

But what is an environment ? An environment is a set of tools installed inside a folder instead of system-wide. Classically, environments are useful when you don't have system administration rights (HPC center, workstation locked by evil sysadmin) or when you have to switch between versions of the same modules.

Environments could be preinstalled by system administrators or built by users on home-directories (local or network).

Why using PhyOcean instead of choosing your products yourself ?
 * Dehydrated software (just add water)
 * Commons envs to share scripts with your colleagues
 * Not only for Python
 * (Tested with our needs) no yet a reality

Two environments are fixed per year (May and November), *fromveur* environment had no fixed versions, so use it with caution.

## Available environments (stable)

### PhyOcean 2023.11
* Codename: `phyocean-2023.11`
* Downloads : [linux](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2023.11.linux.yaml) | [macos](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2023.11.macos.yaml) | [win](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2023.11.win.yaml)

<table>
<tr>
<th> Category </th>
<th> Items </th>
</tr>
</tr>
<td> 🚨 </td>
<td> Python 3.10, JupyterLab 4, Cuda 11.8 (🐧), Dask 2024.2, Numpy 1.26, Pandas 2.2, Tensorflow 2.11, Scikit 1.12, xarray 2024.1, PyFerret </td>
</tr>
</tr>
<td> Python </td>
<td> Cartopy 0.22, matplotlib, holoview, hvplot, Cerbere (🐧), gsw, gpxpy, rasterio, Bokeh, Cython 3.0.8, netcdf4 1.6, wxpython</td>
</tr>
</tr>
<td> Python (data) </td>
<td> Zarr 2.17, intake, s3fs, cdsapi, Cerbere, Google Cloud Storage, ESGF Pyclient, ncview (🐧 and 🍏), NCO Tools, Wekeo hda</td>
</tr>
</tr>
<td> Development </td>
<td> mpi4py 3.1.4, f2py, Gcc/gfortran 12.2, Spyder, nodeJS, Sphinx </td>
</tr>
</table>

### PhyOcean 2023.05
* Codename: `phyocean-2023.11`
* Downloads : [linux](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2023.05.linux.yaml) | [macos](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2023.05.macos.yaml) | [win](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2023.05.win.yaml)

<table>
<tr>
<th> Category </th>
<th> Items </th>
</tr>
</tr>
<td> 🚨 </td>
<td> Python 3.10, JupyterLab 4, Cuda 11.8 (🐧), Dask 2023.5, Numpy 1.24, Pandas 2.0, Tensorflow 2.11, Scikit 1.10, xarray 2023.5, PyFerret </td>
</tr>
</tr>
<td> Python </td>
<td> Cartopy 0.21, matplotlib, holoview, hvplot, Cerbere (🐧), gsw, gpxpy, rasterio, Bokeh, Cython 0.29, netcdf4 1.6, wxpython</td>
</tr>
</tr>
<td> Python (data) </td>
<td> Zarr 2.14, intake, s3fs, cdsapi, Cerbere, Google Cloud Storage, ESGF Pyclient, ncview (🐧 and 🍏), NCO Tools, Wekeo hda</td>
</tr>
</tr>
<td> Development </td>
<td> mpi4py 3.1.4, f2py, Gcc/gfortran 12.2, Spyder, nodeJS, Sphinx</td>
</tr>
</table>


---

## Old environments

Please see [dedicated page](arch.md).

---

## Dev environments (unstable)

### PhyOcean "Fromveur"
* Platform(s) : 🐧 🍏
* Codename: `phyocean-fromveur`
* Downloads : [linux](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-fromveur.linux.yaml) | [macos](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-fromveur.macos.yaml) | [win](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-fromveur.win.yaml)


🚨 Software versions are not pinned. Software/modules could be added or removed... Please read yaml file for details.

## Using PhyOcean envs at LOPS

JupyterHub users, PhyOcean envs are pre-registered on LOPS JupyterHub services ([see LOPS internal docs](https://collab.umr-lops.fr/fr/systeme/moyens-de-calcul/kiosque-jupyter-hub))

LOPS-IUEM users, these environments are available with `module` on workstations or computing facilities.
```
module load envs/phyocean-2021.11
```

## Using PhyOcean envs on your computer

### MicroMamba

⚠️ bash & zsh shell on Linux & OS X only

microMamba is an open-source implementation of Conda, it aims to be lighter and faster than Conda. microMamba is fully compatible with Conda packages, repositories (conda-forge) and environment files.

First, install microMamba, read install instructions from [Mamba documentation](https://mamba.readthedocs.io/en/latest/user_guide/micromamba.html). 

```
micromamba create -f phyocean-2022.05.yaml
```
Next, activate env with
```
micromamba activate phyocean-2022.05
```


### Conda/Anaconda

First, install Anaconda, read install instructions from [Anaconda documentation](https://docs.anaconda.com/anaconda/install/).

Download chosen environment file. Latest stable is [phyocean-2022.05.linux.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-2022.05.linux.yaml) or unfixed [phyocean-fromveur.yaml](https://raw.githubusercontent.com/umr-lops/phyocean-envs/main/envs/phyocean-fromveur.linux.yaml).

```
conda env create -f ~/Downloads/phyocean-2022.05.yaml
```
Next, activate env with
```
conda activate phyocean-2022.05
```
