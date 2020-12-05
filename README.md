# TeachopenCADD_Excercises

This repository contains tutorial from TeachopenCADD website to understand CADD methods.

link: https://projects.volkamerlab.org/teachopencadd/talktorials.html

## chembl webclient  installation
I installed chembl with conda. See below:

	wget https://github.com/volkamerlab/teachopencadd/archive/master.zip -O teachopencadd.zip
	unzip teachopencadd.zip
	cd teachopencadd-master
	conda env create -f environment.yml
	conda activate teachopencadd
	teachopencadd -h

## add jupyter lab extention
	conda install nodejs
	jupyter labextension install @jupyter-widgets/jupyterlab-manager nglview-js-widgets @jupyterlab/toc
 
## check all packages installed
	conda list

## now in case if you face error below even if chEMBL client is installed. This is the general solution if Package/ module is installed but can not be imported in Jupyter notebook.

	Error:
	"No module named 'chembl_webresource_client'"

Solution:
then, check which Python is used in juoyter notebook and in terminal

## commands in terminal:
	"which python"

it should show which python from environment like this "/home/mandar/anaconda3/envs/teachopencadd/bin/python"

## Commands in jupyter notebook:

	!which python

OR

	import sys ; sys.executable

## if both Python excutables are from differnet source then that is the problem

check kernels:

	jupyter kernelspec list

## if Python or environment kernel is absent, add it using this command
	python -m ipykernel install --user --name teachopencadd --display-name "Python (teachopencadd)"

## check kernel of environment
	cat /home/mandar/.local/share/jupyter/kernels/teachopencadd/kernel.json

## Restart notebook and all set !!! 
