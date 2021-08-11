# References and Resources for Neural Recommender Systems Research
This is a repository containing reference materials that may be helpful in jumpstarting your research on neural, review-based recommender systems, with special focus on collaborative filtering. Be sure to click the text in blue (**[like this](#)**) so that you will be redirected to the appropriate reference!

## Prelude: Types of Recommender Systems
* Content-Based Filtering 
* Collaborative Filtering
* Matrix Factorization

Kindly read this **[PPT presentation](https://docs.google.com/presentation/d/12ZJ8eOqyEqvooXTdgwEW13sK2wpKmVLIEMhZ9wRrd0I/edit?usp=sharing)** that details their differences and basic implementations.

## Foundational Neural Recommender Models
### NCF
This time, we will talk about implementing collaborative filtering using deep learning and neural networks AKA neural collaborative filtering (NCF).

Designing a CF model involves two crucial steps or procedures. The first step is learning user and item representations, and the second step is modeling user-item interactions based on the representations mentioned earlier. One of the fundamental works in the utilization of NN in CF is called neural collaborative filtering (NCF) **[(He et al., 2017)](https://dl.acm.org/doi/pdf/10.1145/3038912.3052569?casa_token=PCPE6Y-KhqkAAAAA:8Zf5UV5HKgeUrlBqwitykc8WHpu_0eKVOO8lnNLhun8aON_TvLoQbvIqUFdHOAenjeEwsr57wt6Q7A)**. NCF, originally implemented for implicit feedback data-driven CF, learns non-linear, flexible, and more abstractive interactions between users and items by employing MLP layers as its interaction function. An MLP-based interaction function overcomes the limitations of an inner product-based interaction function. The latter is said to be sub-optimal to learn rich yet complicated patterns from real-world data.

This **[PPT file](https://docs.google.com/presentation/d/1qekyFWgY1jtF4fYHePFVYBYwey7dxz4WtPK4GC8KvM8/edit?usp=sharing)** contains a TL;DR version of the NCF paper. Before continuing any further, it is essential that you carefully understand the concepts and principles surrounding NCF.

### DeepCoNN and NARRE
Arguably, DeepCoNN and NARRE are the first recommender systems that effectively utilize neural networks, thereby leading to state-of-the-art performances.

DeepCoNN is the first deep learning-based model representing users and items from reviews in a joint manner **[(Zheng, Noroozi, & Yu, 2017)](https://dl.acm.org/doi/pdf/10.1145/3018661.3018665)**. The model consists of two parallel networks powered by convolutional neural networks (CNN). One network learns user behavior by examining all reviews he has written, and the other network models item properties by exploring all reviews it has received. A shared layer connects these two networks, and factorization machines capture user-item interactions. 

Another significant model is NARRE, which shares several similarities with DeepCoNN. NARRE is also composed of two parallel CNN-based networks that are uniquely incorporated with the review-level attention mechanism **[(Chen et al., 2018)](https://dl.acm.org/doi/pdf/10.1145/3178876.3186070?casa_token=HgeF0UM2TLsAAAAA:D7yvWV5BxKzkwi3UWdXjfd2IPTa7LdFAU_A801OUe0CbKbULR2iHW5qxRGlGSPZ97NmpgoOAE8uqlg)**. The said mechanism distinguishes each review's usefulness or contribution based on attention weights. As a side-effect, this also leads to review-level explanations; reviews with the highest attention scores are presented as explanations. These weights are then incorporated into the representations of users and items to enhance embedding quality.

## Attention-Based Recommender Models
Before you proceed, make sure that you have a grasp on attention mechanisms.


## BERT-Based Recommender Models
Before you continue, ensure that you are familiar with BERT. There are some helpful video links that discuss BERT by **[CodeEmporium](https://www.youtube.com/watch?v=xI0HHN5XKDo)** and **[Henry AI](https://www.youtube.com/watch?v=OR0wfP2FD3c)**. Keep in mind that BERT is generally used as automatic feature extractors from reviews.  

Notwithstanding, CNN-based approaches fail to consider global context and word frequency information. These two factors are crucial because they can affect recommendation performance. In this regard, **[NCEM](https://ieeexplore.ieee.org/iel7/6287639/8600701/08782556.pdf)** and **[BENEFICT](https://www.aclweb.org/anthology/2020.aacl-main.18.pdf)** replaces the CNN with a pre-trained BERT model in the parallel user/item networks. BERT's advantage lies in its full retention of global context and word frequency information. 
