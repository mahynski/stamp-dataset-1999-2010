Seabird Tissue Archival and Monitoring Project (STAMP) Dataset from 1999-2010
============

This repository contains the raw data and examples of how to process it for selected entries from the STAMP project.
Any mention of commercial products is for information only; it does not imply recommendation or endorsement by NIST.

## Installation

The procedure below uses [conda](https://conda.io/projects/conda/en/latest/index.html) to install package dependencies, which we recommend doing in a separate virtual environment, assumed below to be called "myenv". The python packages in requirements.txt can be installed via other methods as well.

~~~ bash
$ git clone https://github.com/mahynski/stamp-dataset-1999-2010
$ cd stamp-dataset-1999-2010
$ conda activate myenv
$ conda install --file requirements.txt
~~~

## Usage

You can recreate plots found in Ref. [1] using the visualize_stamp.ipynb [Jupyter](https://jupyter.org/) notebook.  The required libraries are included in the requirements.txt and should be installed in the above step.

Otherwise, the included X.csv and y.csv contain the processed chemometric information described in Ref. [1].  The raw data is available at [https://dx.doi.org/10.18434/mds2-2431](https://dx.doi.org/10.18434/mds2-2431).

## Example

This data can be easily read, for example, with [pandas](https://pandas.pydata.org/) in [python](https://www.python.org/):

~~~python
>>> import pandas as pd
>>> X = pd.read_csv('X.csv')
>>> y = pd.read_csv('y.csv')
~~~

## File descriptions

* X.csv : CSV file with the processed chemical information that should be used for analysis.
* y.csv : CSV file with the target properties of each sample, corresponding to X.csv.

## References

[1] Mahynski NA, Ragland JM, Schuur SS, Pugh R, Shen VK, "Seabird Tissue Archival and Monitoring Project (STAMP) Data from 1999-2010," Journal of Research of the National Institute of Standards and Technology, Volume 126, Article No. 126028, https://dx.doi.org/10.6028/jres.126.028
