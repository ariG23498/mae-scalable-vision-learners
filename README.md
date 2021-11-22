# Masked Autoencoders Are Scalable Vision Learners


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ariG23498/mae-scalable-vision-learners/blob/master/mae-pretraining.ipynb)


A TensorFlow implementation of Masked Autoencoders Are Scalable Vision Learners [1]. Our implementation of the proposed method is  available in
[`mae-pretraining.ipynb`](https://github.com/ariG23498/mae-scalable-vision-learners/blob/master/mae-pretraining.ipynb) notebook. It includes evaluation with **linear probing** as well. Furthermore, the notebook can be fully executed on Google Colab.
Our main objective is to present the core idea of the proposed method in a minimal and readable manner.

<div align="center">
  <img src=assets/mae.png/><br>
  <small>Source: <a href=https://arxiv.org/abs/2111.06377>Masked Autoencoders Are Scalable Vision Learners</a></small>
</div><br>


With just **100 epochs** of pre-training and a fairly lightweight and asymmetric Autoencoder architecture we achieve **49.33%%** accuracy
with linear probing on the **CIFAR-10** dataset. Our training logs and encoder weights are released in [`Weights and Logs`](https://github.com/ariG23498/mae-scalable-vision-learners/releases/tag/v1.0.0). 
For comparison, we took the encoder architecture and trained it from scratch (refer to [`regular-classification.ipynb`](https://github.com/ariG23498/mae-scalable-vision-learners/blob/master/regular-classification.ipynb)) in a fully supervised manner. This gave us ~76% test top-1 accuracy.

_We note that with further hyperparameter tuning and more epochs of pre-training, we can achieve a better performance
with linear-probing._  Below we present some more results:

| Config | Masking<br>proportion | LP<br>performance | Encoder weights<br>& logs |
|:---:|:---:|:---:|:---:|
| Encoder & decoder layers: 3 & 1<br>Batch size: 256 | 0.6 | 44.25% | [Link](https://github.com/ariG23498/mae-scalable-vision-learners/releases/download/v1.0.0/44_25.zip) |
| Do | 0.75 | 46.84% | [Link](https://github.com/ariG23498/mae-scalable-vision-learners/releases/download/v1.0.0/46_84.zip) |
| Encoder & decoder layers: 6 & 2<br>Batch size: 256 | 0.75 | 48.16% | [Link](https://github.com/ariG23498/mae-scalable-vision-learners/releases/download/v1.0.0/48_16.zip) |
| Encoder & decoder layers: 9 & 3<br>Batch size: 256<br>Weight deacy: 1e-5 | 0.75 | 49.33% | [Link](https://github.com/ariG23498/mae-scalable-vision-learners/releases/download/v1.0.0/49_33.zip) |

<sup>LP denotes linear-probing. Config is mostly based on what we define in the hyperparameters
section of this notebook: `mae-pretraining.ipynb`.</sup>

## Acknowledgements

* [Xinlei Chen](http://xinleic.xyz/) (one of the authors of the original paper)
* [Google Developers Experts Program](https://developers.google.com/programs/experts/) and [JarvisLabs](https://jarvislabs.ai/) for providing credits to perform extensive experimentation on A100 GPUs.

## References

[1] Masked Autoencoders Are Scalable Vision Learners; He et al.; arXiv 2021; https://arxiv.org/abs/2111.06377.
