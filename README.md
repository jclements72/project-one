This project is a team challenge to study food deserts in the United States using Jupyter notebooks.

The project examines some characteristiscs of food deserts in the United States, differences in rural, urban, and suburban food deserts, and relationships between food desert areas and selected demographic factors.

The Jupyter notebook uses a dataeset from the Economic Research Service of the USDA that was created in 2018 and contains data at different points between 2010 and 2018.  The ERS also produces a Food Environment Atlas describing the data, approximately annually.  Current and archived coies are available on its website.

The project files include a Jupyter notebook, "project_one_maps.ipynb," a PowerPoint presentation, the Excel workbook containing the ErS data, a shapefile of U.S. counties from the US Census Bureau data download cite, an output .csv file of merged data, and  .png files for each of the plots and maps generated.   All input files are in the "input_data" directory, and all images files created are in the "output_data" folder.

A literature survey was conducted prior to and concurrent with code development, and a reference list can be found at the end of the PowerPoint Slides.

The code originally used an API call to the US Census Bureau to get a json of the US counties geometries, but the server was subject to intermitten lack of availabiily, so the script was modified to use a local shapefile instead.

This notebook requires a number of very specific packages be installed, including GeoPandas, plotly express, and fiona. It also requires that an environment variable be set for PROJ_LIB for the project CRS system for pyproj.  The linear regreassinos requre scipy.

As is noted on the package website, installation of geopandas can be complicated and the simplest and cleanest way to install the package is to create a new conda enviroment for geospatial work, and conda install geopandas there.  The process will install a lenghty list of other dependencies, including fiona. 

Although some of its webpages indicate that Fiona is compatible with python 3.7 and no later versions, other webpages explain that in fact it is compatible with later versions of Python.  Any issues with Fiona not being found can be corrected by donig a pip install of Fiona in the geospatial environment. 

To create the static images from the dynmamic maps, the notebook requres orca to be installed in the environment where it is run. 