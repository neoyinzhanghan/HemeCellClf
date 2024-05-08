# HemeCellClf

To train your model run.
```
python scripts/train.py
```
You will have to specify your data path, training resources and hyperparamters in the script/train.py itself at the very beginning of the script.

```
############################################################################
####### DEFINE HYPERPARAMETERS AND DATA DIRECTORIES ########################
############################################################################

default_config = {"lr": 3.56e-07}  # 1.462801279401232e-06}
num_epochs = 500  # 200
data_dir = "/media/hdd2/neo/blasts_skippocytes_split"
num_gpus = 3
num_workers = 20
downsample_factor = 1
```