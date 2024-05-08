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

`lr` is the learning rate. `num_epochs` is the number of epochs. `data_dir` is that path to your data. We assume that `data_dir` has three subfolders `data_dir/train`, `data_dir/val`, `data_dir/test`. Each subdirectory has a number of further subfolders each for a class, and within those folders the cell images in that class.

```
data_dir
    - train
        - M1_normal
            - M1_E2_ER5_MO1 ... .jpg
            - M1_M2_B1_MO1 ... jpg
            ...
        - M1_AML
            ...
    - val
        - M1_normal
            ...
        - M1_AML
            ...
    - test
        - M1_normal
            ...
        - M1_AML
            ...
```

To train with no hang up.
```
nohup python scripts/train.py > train_progress.log 2> train_error.log &
```

The results which include tensorboard as well as checkpoints will be saved in the working directory under subfolder `lightning_logs`.
