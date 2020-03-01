If github in unable to render a Jupyter notebook, copy the link of the notebook and enter into the nbviewer: https://nbviewer.jupyter.org/

# Dimensionality Reduction: An Introduction

Dimensionality reduction is a technique to decrease the complexity of the data by representing it with fewer dimensions. The assumption is that the essence or core content of the data does not span along all dimensions.

It identifies the combination of attributes (principal components, or directions in the feature space) that account for the most variance in data.

For example, consider the following figure. Although x lives in two dimensions, it really occupies a small "lower dimension" in 1D subspace. This lower dimension accounts for the most varince in x.

<img src="https://cse.unl.edu/~hasan/Pics/DimensionalityReduction.png" width=400 height=200>

Thus, it would be useful to represent data in lower dimensions. There are at least two benefits of dimensionality reduction:
- Learning becomes easier because of fewer parameters.
- Enables visualization by projecting data in lower dimension. We can discover “intrinsic dimensionality” of data. We can determine that, for some problems, the high dimensional data is truly lower dimensional.




## Methods for Dimensionality Reduction 

There are two main methods for reducing dimensionality. 
- Feature selection:
        -- We are interested in finding k of the d dimensions that give us the most information and we discard the other (d − k) dimensions.

- Feature extraction: 
        -- We are interested in finding a **new** set of k dimensions that are combinations of the original d dimensions. 

#### In this notebook series we will investigate the feature extraction method of dimensionality reduction.



## Dimensionality Reduction by Feature Extraction

There are two types of feature extraction methods of dimensionality reduction:
- Linear methods
- Non-linear methods


## Linear Methods 

Linear methods of feature extraction for dimensionality reduction could be supervised or unsupervised depending on whether or not they use the output information. 

The best known and most widely used linear methods are:
- Principal Components Analysis (PCA) - unsupervised
- Linear Discriminant Analysis (LDA) - supervised

Two other unsupervised linear projection methods are: Factor Analysis (FA) and Multidimensional Scaling (MDS). 


## Non-Linear Methods 

The linear methods of dimensionality reduction are flexible, fast, and easily interpretable. For example, PCA works well when the data lies in a **linear subspace**. However, this may not hold in many applications when there are **nonlinear relationships** within the data in lower-dimension.

For example, the following dataset is three-dimensional. However, notice that it is created by folding a 2D plane. Thus, the intrinsic lower dimension is 2D. But, the lower-dimension sub-space is **non-linear**!

<img src="https://cse.unl.edu/~hasan/Pics/SwissRoll.png" width=400 height=200>

One approach to resolve this issue is use a non-linear dimensionality reduction technique that is known as Manifold Learning.
In Manifold Learning we assume that the data of interest **lie on an embedded non-linear manifold within the higher-dimensional space**. More generally, a d-dimensional manifold is a part of an n-dimensional space (where d < n) that locally resembles a d-dimensional hyperplane.


We discuss the Manifold Learning non-linear methods in detail in a separate notebook.


### Manifold Learning Algorithms

There are many algorithms for implementing Manifold Learning.

- Locally Linear Embedding (LLE)
- Isometric feature mapping (Isomap)
- Multi-dimensional Scaling (MDS)
- t-distributed Stochastic Neighbor Embedding (t-SNE)

For information on other algorithms and their scikit-learn implementation:
https://scikit-learn.org/stable/modules/manifold.html



## Index for the Notebook Series on Dimensionality Reduction

There are 7 notebooks on Dimensionality Reduction.

- Dimensionality Reduction-1-Linear Methods: Visualize linearly separable data using two linear methods: PCA and LDA

- Dimensionality Reduction-2-Non-Linear Methods-Manifold Learning: Visualize linearly non-separable data using non-linear methods: LLE, Isomap, MDS, t-SNE

- Dimensionality Reduction-3-Introduction to t-SNE

- Dimensionality Reduction-4-Visualize MNIST in 2D using t-SNE: Visualize high-dimensional MNIST data using t-SNE

- Dimensionality Reduction-5-Compression & Decompression Using PCA: Perform data compression & decompression using PCA and investigate the effect of PCA on a classification algorithm

- Dimensionality Reduction-6-Incremental PCA: How to apply apply PCA on a very large dataset and in active learning using incremental PCA

- Dimensionality Reduction-7-Kernel PCA: Visualize linearly non-separable data using Kernel PCA
