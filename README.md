# UniAug

This is the code base for the UniAug project.

## Enviroment Requirements.

```bash
conda create -f graph_enviroment.yaml
conda activate graph
pip install -r requirements.txt
pip install -f https://data.pyg.org/whl/torch-2.1.0+cu121.html torch-cluster==1.6.3+pt21cu121 torch-scatter==2.1.2+pt21cu121 torch-sparse==0.6.18+pt21cu121 torch-spline-conv==1.2.2+pt21cu121
pip install git+https://github.com/fabriziocosta/EDeN.git --user

```

After executing the shell commands above, there should be a conda enviroment named graph with all dependencies.


## Running Shell Scripts.

All of our shell scripts are under the `run` folder to ease usage.
If you are using HPC,you may need to revise the Resource Request part for scripts with the prefix `hpcc` correspondingly.

Kindly note that for the very first time you may need to login wandb before the execution via `wandb login` following the prompts.

### Graph Prediction

You could uncomment the corresponding linesin the scripts for different datasets and guidence settings.

```shell
bash run/graph_pred_mol.sh
```

### Node Classification

You could uncomment the corresponding linesin the scripts for different datasets and guidence settings.

```shell
bash run/node_class_subgraph.sh
```


### Link Prediction

You could uncomment the corresponding lines for different datasets and guidence settings.
```shell
bash bash run/link_pred_ncn.sh
```
