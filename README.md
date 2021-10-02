# Domain-Adaptation-by-Unilateral-Alignment
Domain adaptation involves transferring the learned knowledge from the source domain to the target domain. The existing approaches assume an identical label space between both source and target domains which poses limitations in real-world applications when there are missing classes in the target training set. So the two-stage unilateral approach mitigates this problem by making use of the inter-class relationships of the source domain and aligns unilaterally the target to the source domain. The approach is evaluated on the MNIST to MNIST-M adaptation.

I've tried to re-implement the proposed architecture in 2001.02015.pdf (arxiv.org) using Keras with TensorFlow backend.

The datasets used are MNIST and MNIST-M

MNIST-M: https://github.com/VanushVaswani/keras_mnistm/releases/download/1.0/keras_mnistm.pkl.gz
