This is a short walkthrough on setting up a *generic* geospatial analysis Anaconda environment on your  machine.

This also installs the Jupyter Notebook software commonly used for Python (and other) development tasks.

Please let Marziya Farooq (mfarooq1@worldbank.org) know if any changes are required!

-----------------------------------

1. Install Anaconda
2. Open Anaconda Powershell

3. Run the following commands *in this order*

conda create --name geoen python=3.11.8
conda activate geoen

conda install -n base conda-libmamba-solver

conda install vs2015_runtime=14 --solver=libmamba

conda install -c conda-forge pandas geopandas rasterstats rasterio geojson regex numpy --solver=libmamba

conda install -c conda-forge shapely fiona matplotlib GDAL requests rasterstats rioxarray xarray os --solver=libmamba

pip install mercantile

pip install quadkey

pip install tqdm

conda install dask

pip install wheel

pip install GDAL

pip install ipykernel jupyterlab rioxarray

python -m ipykernel install --user --name geoen --display-name "Python (geoen)"
