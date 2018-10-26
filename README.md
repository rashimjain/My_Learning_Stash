# My_Learning_Stash

## 1. Merging Multiple Jupyter Notebooks 

nbmerge: merge / concatenate Jupyter notebooks

Installation

pip install nbmerge
Usage

For the usage as originally specified by @fperez's gist,

nbmerge file_1.ipynb file_2.ipynb file_3.ipynb > merged.ipynb
Alternatively, nbmerge can cursively collect all files in the current directory and below, recursively. After collection, it sorts them lexicographically. You can use a regular expression as a file name predicate. All .ipynb_checkpoints are automatically ignored. And, you can use the -i option to ignore any notebook prefixed with an underscore (think pseudo-private in python).

For example, the following command collects all notebooks in your project that have the word intro in the file name and saves it to a merged file named _merged.ipynb,

nbmerge --recursive -i -p ".*intro.*" -o _merged.ipynb
