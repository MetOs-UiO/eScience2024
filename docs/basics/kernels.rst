Using different kernels in notebooks
====================================


  .. note::
     We are using ``mamba`` here which you can substitute with ``conda`` if you wish to use anaconda instead. 

We provide different conda environments as kernels for processing jupyternotebooks.
You can see them in the launcher when you create a new notebook or choose one in the drop-dowmn menu in the top right corner.

If you want to check which packages are included in the environment you can find the names of the environments available by doing: ``mamba env list``.
To list packages and their versions within the environment use the following command: ``mamba list -n environment_name --export``.
You can also pipe it to a file to view later or to create same environment somwhere else: ``mamba list -n environment name --export > environment.txt``
To create an environment out of this file: ``mamba -n environment_name -f environment.txt``. 

  .. note::
     The exported environment is platform specific, f.e. you will see ``platform: linux-64``.
     Recreating the environment on another platform might not work since some of the packages might not be available for your target platform.
     In that case, it's recommended to use containers to reproduce the environment.

Available kernels
-----------------

- **Base**: contains basic packages (mostly not useful for data processing)
- **Pangeo**: environment, built from `Pangeo nootbook v2024.04.05 <https://github.com/pangeo-data/pangeo-docker-images/tree/2024.04.05/pangeo-notebook>`_
- **Ml-notebook**: environment, built from `Pangeo ml-nootbook v2024.04.05 <https://github.com/pangeo-data/pangeo-docker-images/tree/2024.04.05/ml-notebook>`_ with added packages:

  .. code-block::

    'gpflow' 
    'scikit-learn'
    'tf-keras'
    'tensorflow-probability'
    'tensorflow'
    'iris'
    'tqdm'

- **Python3.9**: environment with packages:

  .. code-block::

    'python==3.9.19' 
    'pycel'
    'ipykernel' 
    'scikit-learn'
    'netcdf4'
    'xarray' 
    'pyngl' 
    'proplot' 
    'cartopy' 
    'rioxarray' 
    'assimulo' 
    'pandas' 
    'proplot' 
    'seaborn' 
    'cis'
