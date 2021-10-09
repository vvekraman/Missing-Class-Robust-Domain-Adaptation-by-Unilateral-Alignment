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
| 0->1    |     96.36 ± 0.81 |                            68.43 |
| 0->2    |                - |                            - |
| 0->3    |                - |                            - |
| 1->0    |                - |                            - |
| 1->2    |                - |                            - |
| 1->3    |                - |                            - |
| 2->0    |                - |                            - |
| 2->1    |                - |                            - |
| 2->3    |                - |                            - |
| 3->0    |                - |                            - |
| 3->1    |                - |                            - |
| 3->2    |                - |                            - |
