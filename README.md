# Missing-Class-Robust-Domain-Adaptation-by-Unilateral-Alignment
Domain adaptation involves transferring the learned knowledge from the source domain to the target domain. The existing approaches assume an identical label space between both source and target domains which poses limitations in real-world applications when there are missing classes in the target training set. So the two-stage unilateral approach mitigates this problem by making use of the inter-class relationships of the source domain and aligns unilaterally the target to the source domain. The approach is evaluated on the MNIST to MNIST-M adaptation.

I've tried to re-implement the proposed architecture on the paper "Missing-Class-Robust Domain Adaptation by
Unilateral Alignment for Fault Diagnosis" (https://arxiv.org/pdf/2001.02015.pdf) using Keras with TensorFlow backend.

The datasets used are MNIST, MNIST-M and CWRU

MNIST-M: https://github.com/VanushVaswani/keras_mnistm/releases/download/1.0/keras_mnistm.pkl.gz

CWRU (12khz-SR): https://drive.google.com/file/d/1Ll7wfNrjtbZbM8RehdXtGkUKBbX8mNTT/view?usp=sharing

Obtained accuracy on test_set(MNISTM) (trained for 50 epochs):
| Missing_classes   |   Accuracy(%)(paper) |   Accuracy(%)(re-implementation) |             
|-------------------|----------------------|----------------------------------|
| 0/10              |                76.74 |                            58.20 |
| 2/10              |                75.03 |                            57.72 |
| 8/10              |                74.06 |                            54.55 |


Obtained accuracy on CWRU target data (trained for 50 epochs):
|Tasks|   Accuracy(%)(paper) |   Accuracy(%)(re-implementation) |             
|---------|------------------|----------------------------------|
| 0->1    |     96.36 ± 0.81 |                            66.76 |
| 0->2    |     97.38 ± 1.66 |                            62.02 |
| 0->3    |     95.78 ± 1.90 |                            67.21 |
| 1->0    |     97.49 ± 0.52 |                            69.02 |
| 1->2    |     99.94 ± 0.04 |                            70.46 |
| 1->3    |     99.58 ± 0.15 |                            68.46 |
| 2->0    |     93.77 ± 2.09 |                            69.64 |
| 2->1    |     97.60 ± 0.36 |                            71.60 |
| 2->3    |     99.86 ± 0.08 |                            72.62 |
| 3->0    |     88.42 ± 0.72 |                            68.88 |
| 3->1    |     93.45 ± 1.68 |                            67.74 |
| 3->2    |     99.83 ± 0.06 |                            67.35 |
