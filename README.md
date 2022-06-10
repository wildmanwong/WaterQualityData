# WaterQualityData
EPA collects water monitoring data.  For those that are interested in analyzing the data but have more limited computer resources (disk, RAM) for preprocessing we are making a reduced set of data (1900-2022) readable in a pandas format (parquet file).  You can download the original data for the physical/chemical and biological data from https://www.epa.gov/waterdata/water-quality-data-download in csv format (86 GB compressed, 489 GB uncompressed)


Directory smallData - only contains the following data (423M entries):
- OrganizationFormalName
- ActivityStartDate
- ActivityLocation/LatitudeMeasure
- ActivityLocation/LongitudeMeasure
- CharacteristicName
- ResultMeasureValue
- ResultMeasure/MeasureUnitCode
- State

The phy.gzip file contains the physical/chemical data (2.6 GB compressed, 9.4 GB in RAM)

The bio.gzip file contains the physical/chemical data (3.9 GB compressed, 5.8 GB in RAM)


To read the file(s) use something like this:

df = pandas.read_parquet('phy.gzip')
