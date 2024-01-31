 Inference attacks aim to obtain knowledge about the dataset that was used to train a victim model. In this guide, we are going to try model inversion — an attack where the adversary tries to recover the training dataset of the victim model.

As of version 1.10.0, ART supported only one model inversion algorithm — MIFace. MIFace uses class gradients to infer the training dataset.