# ogbn-products

This repository includes the following example scripts:

* **[MLP](https://github.com/snap-stanford/ogb/blob/master/examples/nodeproppred/products/mlp.py)**: Full-batch MLP training based on product features and optional Node2Vec features (`--use_node_embedding`). For training with Node2Vec features, this script requires node embeddings be saved in `embedding.pt`. To generate them, please run `python node2vec.py`.
* **[Full-batch GCN](https://github.com/snap-stanford/ogb/blob/master/examples/nodeproppred/products/full_batch.py)**: Full-batch GNN training using either the GCN or GraphSAGE operator (`--use_sage`). This script will require large amounts of GPU memory.
* **[Cluster-GCN](https://github.com/snap-stanford/ogb/blob/master/examples/nodeproppred/products/cluster_gcn.py)**: Mini-batch GCN training using the Cluster-GCN algorithm. Cluster-GCN examples require PyTorch Geometric >= 1.4.3.
* **[GraphSAINT](https://github.com/snap-stanford/ogb/blob/master/examples/nodeproppred/products/graph_saint.py)**: Mini-batch GCN training using the GraphSAINT algorithm. GraphSAINT examples require PyTorch Geometric master.
* **[SIGN](https://github.com/snap-stanford/ogb/blob/master/examples/nodeproppred/products/sign.py)**: Training using pre-computed GNN representations using Scalable Inception Graph Neural Networks (SIGN). SIGN examples require PyTorch Geometric master.

## Training & Evaluation

```
# Run with default config
python cluster_gcn.py

# Run with custom config
python cluster_gcn.py --hidden_channels=128
```
