# Rd2SphinxRst

Rd2SphinxRst converts Rmarkdown (.Rd) files generated Roxygen2 to Rst files that can be processed by Sphinx to build a documentation webpage.

## Usage

The main entry point is the file `Rd2SphinxRst.py`

For example to run the code to generate Rst files for some Rd files in the folder `~/Desktop/mxnet/man/` according to the toctree configuration specified in `~/Desktop/mxnet/toctree` and saved to `~/Desktop/mxnet/doc2/`, you use the command:

`python Rd2SphinxRst.py ~/Desktop/mxnet/man/ ~/Desktop/mxnet/toctree ~/Desktop/mxnet/doc2/ --url http://github.com/apache/incubator-mxnet/blob/master/`

## Contents

### `Rd2SphinxRst.py`
The main entry point accepts a path containing Rd files generated by Roxygen2, JSON toctree configuration and a path to save the generated Rst files.

### `src/man_reader.py`
Defines a python object that accepts a path and reads all the Rd files in the path

### `src/rd_reader.py`
Defines a python object to read individual Rd files and other helper methods

### `src/toctree_reader.py`
Reads a JSON configuration file describing the toctree and can write a corresponding Rst file.


### `src/rst_builder.py`
Builds an Rst file from an RDReader.

