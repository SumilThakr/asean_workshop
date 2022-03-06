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

