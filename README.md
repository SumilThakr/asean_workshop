# Test files for the Global InMAP Model Training in Southeast Asia

Here, you will find all the input files needed to run Global InMAP for the test region in Southeast Asia.

The files include:
- sampleConfig.toml. This is the "configuration file" which tells the model all of the input parameters for a simulation.

- test_emis.shp and associated files. These are the test emission inputs to the model, saying how much pollution is being emitted, what chemical pollutants are being emitted (e.g., sulfur oxides), and where the pollution is being emitted. This is in the ESRI Shapefile format, but gridded inputs (NetCDF) work also.

- test_grid.gob.zip. This is a compressed file containing the grid for the test region. It includes all the input data for InMAP (including atmospheric and meteorological parameters) already processed onto the InMAP grid for the test region.

Using these input files, and given a successful installation of InMAP, one can run:
  ``` bash
  inmap run steady -s --config=sampleConfig.toml
  ```
Which will generate results in Shapefile format (`inmap_test_results.shp`) showing estimates of the annual-average change in PM2.5 concentrations across the test region predicted by InMAP. On my laptop, it takes about 7 minutes and ~1 GB of memory to complete the simulation.

- inmap_test_results.shp and associated files. These are pre-generated outputs from the simulation. The log file, `inmap_test_results.log`, shows the log output of the InMAP simulation.

# InMAP Modelling for the whole ASEAN region

The grid file, `test_grid.gob.zip`, is only for simulations in a test region suitable for this workshop. the InMAP grid for the entire ASEAN region can be downloaded from [here](https://drive.google.com/file/d/1VBXwT0EPHKgrVhV_axgMxf1_9g_Xw7Rp/view?usp=sharing).

# Installing InMAP.

InMAP can be installed by following instructions on the [main GitHub page](https://github.com/spatialmodel/inmap). In the workshop, we will be downloading the most recent release of InMAP suitable for your machine (Windows, OS X or Linux) from the [releases page](https://github.com/spatialmodel/inmap/releases). In that case, the command to run InMAP will instead be something like
 ``` bash
  inmap-v1.9.5-darwin-amd64 run steady -s --config=sampleConfig.toml
  ```
