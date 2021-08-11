# References and Resources for Neural Recommender Systems Research
This is a repository containing reference materials that may be helpful in jumpstarting your research on neural recommender systems, with special focus on collaborative filtering.

## Prelude: Types of Recommender Systems
* Content-Based Filtering 
* Collaborative Filtering
* Matrix Factorization

Kindly read this [PPT presentation](https://docs.google.com/presentation/d/12ZJ8eOqyEqvooXTdgwEW13sK2wpKmVLIEMhZ9wRrd0I/edit?usp=sharing) that details their differences and basic implementations.

## Foundational Neural Recommender Models
### NCF
This time, we will talk about implementing collaborative filtering using deep learning and neural networks AKA neural collaborative filtering (NCF).

Designing a CF model involves two crucial steps or procedures. The first step is learning user and item representations, and the second step is modeling user-item interactions based on the representations mentioned earlier [He et al. (2018)](https://arxiv.org/pdf/1808.03912.pdf). One of the fundamental works in the utilization of NN in CF is called neural collaborative filtering (NCF) [He et al. (2017)](https://dl.acm.org/doi/pdf/10.1145/3038912.3052569?casa_token=PCPE6Y-KhqkAAAAA:8Zf5UV5HKgeUrlBqwitykc8WHpu_0eKVOO8lnNLhun8aON_TvLoQbvIqUFdHOAenjeEwsr57wt6Q7A). NCF, originally implemented for implicit feedback data-driven CF, learns non-linear, flexible, and more abstractive interactions between users and items by employing MLP layers as its interaction function. An MLP-based interaction function overcomes the limitations of an inner product-based interaction function. The latter is said to be sub-optimal to learn rich yet complicated patterns from real-world data.

This [PPT](https://docs.google.com/presentation/d/1qekyFWgY1jtF4fYHePFVYBYwey7dxz4WtPK4GC8KvM8/edit?usp=sharing) contains TL;DR version of the NCF paper. Before continuing any further, it is essential that you carefully understand the concepts and principles surrounding NCF.

### DeepCoNN and NARRE
DeepCoNN is the first deep learning-based model representing users and items from reviews in a joint manner \cite{zheng2017joint}. The model consists of two parallel networks powered by convolutional neural networks (CNN). One network learns user behavior by examining all reviews he has written, and the other network models item properties by exploring all reviews it has received. A shared layer connects these two networks, and factorization machines capture user-item interactions. Another significant model is NARRE, which shares several similarities with DeepCoNN. NARRE is also composed of two parallel CNN-based networks that are uniquely incorporated with the review-level attention mechanism \cite{chen2018neural}. The said mechanism distinguishes each review's usefulness or contribution based on attention weights. As a side-effect, this also leads to review-level explanations; reviews with the highest attention scores are presented as explanations. These weights are then incorporated into the representations of users and items to enhance embedding quality.

## Other Recent Recommender Models
