# Masked Autoencoders Are Scalable Vision Learners


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ariG23498/mae-scalable-vision-learners/blob/master/mae-pretraining.ipynb)


A TensorFlow implementation of Masked Autoencoders Are Scalable Vision Learners [1]. Our implementation of the proposed
method is  available in [`mae-pretraining.ipynb`](https://github.com/ariG23498/mae-scalable-vision-learners/blob/master/mae-pretraining.ipynb)
notebook. It includes evaluation with **linear probing** as well. Furthermore, the notebook can be fully executed on Google Colab.
Our main objective is to present the core idea of the proposed method in a minimal and readable manner.

<div align="center">
  <img src=assets/mae.png/><br>
  <small><a href=https://arxiv.org/abs/2111.06377>Masked Autoencoders Are Scalable Vision Learners</a></small>
</div><br>


With just **100 epochs** of pre-training and a fairly lightweight Autoencoder architecture we achieve **43.57%** accuracy
with linear probing on the **CIFAR-10** dataset. Our training logs and encoder weights are available inside the
[`encoder_weights_logs`](https://github.com/ariG23498/mae-scalable-vision-learners/tree/master/encoder_weights_logs) directory. 

_We note that with further hyperparameter tuning and more epochs of pre-training, we can achieve a better performance
with linear-probing._  We plan on adding results from a few more experiments that we are conducting. So, keep
an eye out :)

## Acknowledgements

* Xinlei Chen (one of the authors of the original paper)
* [Google Developers Experts Program](https://developers.google.com/programs/experts/)
* [JarvisLabs](https://jarvislabs.ai/) for providing credits to perform extensive experimentation on A100 GPUs.

## References

[1] Masked Autoencoders Are Scalable Vision Learners; He et al.; arXiv 2021; https://arxiv.org/abs/2111.06377.
