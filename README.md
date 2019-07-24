# ArtGAN
This is a July 2019 attempt to run the original [ArtGAN](https://github.com/cs-chan/ArtGAN) implementation using up-to-date libraries (tensorflow==1.14, scipy==1.2.2)

Origial paper: https://arxiv.org/abs/1702.03410

# Setup
- Install `python 2.7`
- Install compatible versions of tensorflow-gpu and CUDA. We used CUDA 10.1 and cuDNN 7.5, which are the version requirements for tensorflow==1.14+.
- Install the GPU version of tensorflow: `pip install tensorflow-gpu`
- If the environment var `LD_LIBRARY_PATH` is not set, set it to include shared cudn library files: `LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH` 

# Tips
- To monitor GPU usage, run in a separate terminal:
`watch -n 1 nvidia-smi`

# Weights
The published weights from training on Wikiart (Style) are available at [this https URL](https://drive.google.com/file/d/1PL9zC9i9Cww8sD2uq00el1fz5HjeTlaP/view?usp=sharing)
To generate art with these weights, place the unzipped files here `ArtGAN/ArtGAN/models/Style128GANAE/` and run `python2 Style128GANAEsample.py`
