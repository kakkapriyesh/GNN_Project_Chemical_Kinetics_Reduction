Graphs for reduced order chemical kinetics
======================================
This project was done as a course project for ACMS 80770
A systematic approach for chemical reaction mechanism reduction was developed
and demonstrated. The approach consists of the use of reduction mechanism
approaches such as directed relation graphs (DRG) and directed relation graphs
with error propagation (DRGEP). Both of these approaches are executed using
graph search algorithms. DRG uses a depth-first search algorithm while DRGEP
uses Dijkstra’s algorithm in a modified form to obtain clusters of relevant species
to the target species.



## Getting Started

### Dependencies

This implementation requires:

* Cantera==2.6.0
* matplotlib==3.5.2
* numpy==1.23.1
* networkx==2.8.4
* python==3.10.4

### Installation

After downloading the code, you need to install python ver 3.10 and then installing dependencies in requirements.txt using pip

```bash
conda create -n <env_name> python=3.10
```
```bash
pip install -r requirements.txt
```

### Run and Data 

Data is generated by running DRG.py and DRGEP.py for autoignition problem. 

```bash
python DRG.py
```
```bash
python DRGEP.py
```
To test these reduced species model with premixed flames, use reduced_drg_xx.cti file generated by these graph methods as inputs in 'inp_file' list in 'premixed_flame.py'. Here, xx is the number of species after model reduction. Then run premixed flame
```bash
python premixed_flame.py
```

