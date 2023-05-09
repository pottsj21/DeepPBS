# DeepPBS

![alt text](https://github.com/timkartar/DeepPBS/blob/main/run/figs/Fig1_white.png?raw=true)

Developement Environment:

* Biopython 1.79
* datetime 
* matplotlib 3.5.2
* scipy 1.7.3
* scikit-learn 1.1.1
* pytorch 1.12.1+cu116
* pytorch_geometric 2.1.0
* tqdm 4.64.0
* glob2 0.7
* igl 2.2.1
* json
* logomaker 0.8
* networkx 2.8.4
* pandas 1.4.4
* seaborn 0.11.2
* trimesh 3.10.0
* numpy 1.21.5
* freesasa 2.1.0

## Installation

```
git clone https://github.com/timkartar/DeepPBS
cd deepPBS
pip install .
```

## Quickstart

Pre-trained models are provided with the package.

Example pipeline for processing and predicting is as below:
```
cd deeppbs/run/process

// process and predict the structures present in `deeppbs/run/process/pdb` directory
// see process_config.json and pred_config.json for parameters and path details (note some
parameters are unused) and `proc_source.sh` for required environment setup
// outputs will be generated in `deeppbs/run/process/output` directory

./process_and_predict.sh

// run interpretation on an example pdb file present in `deeppbs/run/process/pdb` (provided it has 
// been processed to an npz file in `deeppbs/run/process/npz`) see `interpret_config.json` 
// output wil be generated in `deeppbs/run/plot_scripts/interpret_output/`

./vis_interpret.sh 5x6g
```

![output](https://github.com/timkartar/DeepPBS/assets/16060117/ff99b40a-432b-43ff-a2c5-b0bde06c2db5)
