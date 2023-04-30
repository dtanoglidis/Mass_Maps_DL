## Cosmological inference from Weak Lensing Mass maps with Deep Learning

Repository containing code for the inference of cosmological parameters (with uncertainty quantification) from simulated mass maps.

We use three different approaches for cosmological parameter inference:

- Standard Convolutional Neural Networks (CNNs).
- Bayesian Neural Networks (BNNs).
- Neural Posterior Estimation (NPE), a Simulation-Based Inference (SBI) method.

All codes were run on Google Colab (Pro version, that gives better access to GPUs) GPUs, with high-RAM requirements. They can easily be adapted for use in different environments. The jupyter notebooks contain detailed descriptions of what they do, but here is a short description, to help you navigate the code:


### Notebook Descriptions:

- [SBI_Convergence_Maps.ipynb](SBI_Convergence_Maps.ipynb) is used to train a NPE (Simulation-Based Inference) model, and produce a file containing predictions on the test set.
- [BNN_Convergence_Maps.ipynb](BNN_Convergence_Maps.ipynb) is used to train a BNN model, and produces a file containing predictions on the same test set as the NPE model.
- [Evaluation_and_Calibration.ipynb](Evaluation_and_Calibration.ipynb) reads the predictions generated using the previous two notebooks and produces posterior examples and calibration plots. We can also use it to generate plots 


Auxillary notebooks:

- [Noisify.ipynb](Noisify.ipynb), adds shape noise to the noiseless maps and produces as an output a file containing noisy maps.
- [Reshuffle_and_Split.ipynb](Reshuffle_and_Split.ipynb), reshuffles and splits the big cosmogrid dataset for faster training/memory requirements.
