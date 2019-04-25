# DVA6242_GroupProject

## Project

All the code for the project contained in the `./CODE` directory.

## Data Files to Download

### Raw Unique Institution Names
Download: https://drive.google.com/file/d/1lKwpA3zjHrVqNqjMds_jAscbyeL4i-Qb/view

### Clustering of the Institution Names
This process operated off the original data file to get a list of fields by paper.
Because of the severe size & time required to set this up, we have replicated the final step of this which is the simplification from specific fields to the general 13 that we constructed.
Download: https://drive.google.com/file/d/1doD_s5MXSSc0jFReCaajA_j_4sEiTXJC/view

#### Requirements
* Python 3 with Packages: Numpy, Pandas and SKlearn
* Jupyter 

#### Steps
1. Navigate to `DVA6262_GroupProject/`
2. Run the clustering notebook via `jupyter notebook clusters.ipynb`
3. Set the `input_filename` variable to the path to the unique institution names.
4. Set the `mapping_filename` and `label_filename` to anything. Make sure that the path to the files exist. 
4. Run the cells.

## Mapping the Fields of Study

#### Requirements
* Python 3

#### Steps
1. Navigate to `DVA6262_GroupProject/fos/`
2. Run script via `python map.py simplified_fields.txt > $output_file`
3. Field names are converted to ID values specified ub FOSIDMAP.txt via bash script `replace.sh`
3. This output is merged with the institution data and sent to Hadoop MapReduce

## Vizualizing the results (Visualization)
#### Requirements
* A http server. [This](https://www.npmjs.com/package/http-server) was used when testing. Alternatively, a program such as [Brackets](http://brackets.io/) can be used to run the vizualization. 
* A browser

#### Steps
1. Navigate to `DVA6262_GroupProject/viz/data/`
2. Extract the 2 zip files in `DVA6262_GroupProject/viz/data/` if `edgefile.csv` and `labels_clusters.csv` are not in the folder.
3. Navigate to `DVA6262_GroupProject/viz/`
4. Start the http server i.e `http-server` and open `graph.html` in your browser.
