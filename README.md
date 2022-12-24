# GDA-Overview
[**Towards Data Augmentation in Graph Neural Network: An Overview and Evaluation**](https://www.sciencedirect.com/science/article/pii/S1574013722000612?via%3Dihub)


Many studies on Graph Data Augmentation (GDA) approaches have emerged. The techniques have rapidly yielded performance improvement for various graph neural network (GNN) models that increase the current state of the art accuracy by absolute values of 4.20\%, 5.50\%, and 4.40\% on Cora, Citeseer, and PubMed, respectively. The success is attributed to two integral properties of relational approaches: topology-level and feature-level augmentation. This work provides an overview of some GDA algorithms which are reasonably categorized based on these integral properties. Next, we engage the three most widely used GNN backbones (GCN, GAT, and GraphSAGE) as plug-and-play methods for conducting experiments. We conclude by evaluating the algorithm's effectiveness to demonstrate significant differences among various GDA techniques based on accuracy and time complexity with additional datasets different from those used in the original works. 

Ultimately, everything can not be captured in one paper. However, we will try to make this list updated. For any issue or uncovered paper under the two listed categories , please don't hesitate to open an issue or pull request.

# Two Integral Properties of Relational Approach in GDA
Before delving to these integral properties, lets list some algorithms and augmentation types used relative to the part considered in the graph data.

| Method   | Type           | Considered Part | Perturbed Part | 
| :---     | :---:          | :---:           | :---:          | 
| AdaEdge  | Sampling       | A               | A              |
| DROPEDGE | Sampling       | A               | A              | 
| GAUG-O   | Reconstruction | A&X             | A              | 
| G-GNN    | Reconstruction | A&X             | X              | 
| LA-GNN   | Generation     | A&X             | X              | 
| NodeAug  | Sampling       | A&X             | X              |
| FLAG     | Generation     | X               | X              | 
| GCA      | Generation     | A&X             | A              | 


## Topology-level Augmentation
We formulate topology-level augmentation as:

$\textbf{A}^{\prime} = \mathcal{H}_{\varphi}(\textbf{X}, \textbf{A})$  

1. DropEdge: Towards Deep Graph Convolutional Networks on Node Classification. [[Paper]](https://arxiv.org/abs/1907.10903) with [[Code]](https://github.com/DropEdge/DropEdge)
2. AdaEdge: Measuring and Relieving the Over-Smoothing Problem for Graph Neural Networks from the Topological View. [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/5747)
3. GAug: Data augmentation for graph neural networks. [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/17315) with [[Code]](https://github.com/zhao-tong/GAug)
4. GCA: Graph contrastive learning with adaptive augmentation. [[Paper]](https://arxiv.org/abs/2010.14945) with [[Code]](https://github.com/CRIPAC-DIG/GCA)
5. ...


## Feature-level  Augmentation
We formulate feature-level augmentation as:

$\textbf{X}^{\prime} = \mathcal{H}^{\varphi}(\textbf{X}, \textbf{A})$

1. Nodeaug: Semi-supervised node classification with data augmentation. [[Paper]](https://dl.acm.org/doi/10.1145/3394486.3403063)
2. FLAG: adversarial data augmentation for graph neural networks. [[Paper]](https://arxiv.org/abs/2010.09891) with [[Code]](https://github.com/devnkong/FLAG)
3. G-GNN: Pre-train and learn: Preserving global information for graph neural networks. [[Paper]](https://arxiv.org/abs/1910.12241) with [[Code]](https://github.com/zhudanhao/G-GNN)
4. LAGNN: Local Augmentation for Graph Neural Networks. [[Paper]](https://arxiv.org/abs/2109.03856) with [[Code]](https://github.com/SongtaoLiu0823/LAGNN)
5. ...
