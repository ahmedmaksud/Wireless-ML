# Wireless-ML

Machine-learning experiments for wireless communication.

## CSI compression & denoising with a convolutional autoencoder

[`autoencoder_CSI_compression.ipynb`](autoencoder_CSI_compression.ipynb) trains a convolutional autoencoder that jointly **compresses and denoises** massive-MIMO Channel State Information (CSI), following [CsiNet](https://ieeexplore.ieee.org/document/8322184).
The CSI matrix is treated as a two-channel (real/imaginary) image.

- **Data** — CSI from the COST 2100 channel model (indoor/outdoor), as used in CsiNet.
- **Models** — a CNN autoencoder (Model 1), a shallower variant (Model 2), and an MSE-loss variant (Model 3).
- **Evaluation** — reconstruction error `MSE = E[(X − X')²]`.

### Running it

Open the notebook in Jupyter and run it top to bottom.
Requires `tensorflow`/`keras`, `numpy`, `scipy`, `matplotlib`, and `seaborn`.

### Reference

C.-K. Wen, W.-T. Shih, and S. Jin, "Deep Learning for Massive MIMO CSI Feedback," *IEEE Wireless Communications Letters*, 2018. — [CsiNet](https://ieeexplore.ieee.org/document/8322184)
