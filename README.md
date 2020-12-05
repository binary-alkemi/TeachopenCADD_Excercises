# TeachopenCADD_Excercises

This repository contains tutorial from TeachopenCADD website to understand CADD methods.

link: https://projects.volkamerlab.org/teachopencadd/talktorials.html

## chembl webclient  installation
I installed chembl with conda. See below:

## create environment
conda create -n teachopencadd -c chembl chembl_webresource_client python=3.8 

#activae environment
conda activate teachopencadd

## install additional packages
conda install -c rdkit 
conda install jupyter
 
# check all packages installed
conda list

# now in case if you face error below even if chEMBL client is installed. This is the general solution if Package/ module is installed but can not be imported in Jupyter notebook.

Error:
"No module named 'chembl_webresource_client'"

Solution:
then, check which Python is used in juoyter notebook and in terminal

## commands in terminal:
"which python"

it should show which python from environment like this "/home/mandar/anaconda3/envs/teachopencadd/bin/python"

# Commands in jupyter notebook:

!which python

	OR

import sys ; sys.executable

## if both Python excutables are from differnet source then that is the problem

check kernels:

jupyter kernelspec list
# if Python is absent / environment kernel, add it using this command
python -m ipykernel install --user --name teachopencadd --display-name "Python (teachopencadd)"
## check kernel of environment
cat /home/mandar/.local/share/jupyter/kernels/teachopencadd/kernel.json

## Restart notebook and all good.
