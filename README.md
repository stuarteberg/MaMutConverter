# MaMut Converter

A converter for visualising ilastik projects in the MaMut plugin(Fiji/ImageJ). 

Usage:

1. Save the raw images as HDF/XML file

	1. open Fiji 
	2. import your raw image data 

				- use the hdf5 plugin, when your data is in HDF5 format (Help -- Update Fiji -- HDF5) 
				
	3. open BigDataViewer Plugin -> Export current Image as XML/HDF5

				- the XML and HDF5 should be in the same folder
				- the name and path of the XML are input-parameters for the script in 2 (input-xml, xml-dir)

2. Execute the hdf_to_xml.py script

	```bash 
	python hdf_to_xml.py
	``` 

	parameters: `--input-dir: path to the event sequence folder 
				`--input-raw: filepath to the HDF5 raw file 
				`--raw-filepath: filepath in the HDF5 raw file
				`--output-dir: folder where the file should be saved
				`--input-xml: name of the input xml from 1 
				`--xml-dir: path to the input-xml (needs to be seperated)
				`--is-3D: 1 if the input is in 3D (default 0)
				`--axes-order-raw: the axes order of the raw input (default txyzc)
				`--axes-order-label: axes order of the label input (default xyzc, without t)

3. Open the output.xml with MaMut