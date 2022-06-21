FROM nvidia/cuda:11.6.2-cudnn8-devel-ubuntu20.04

RUN apt-get update && apt-get install -y \
  git \
  python3 \
  python3-pip \
  && rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade https://storage.googleapis.com/jax-releases/cuda11/jaxlib-0.3.10+cuda11.cudnn82-cp38-none-manylinux2014_x86_64.whl \
  && pip install -q \
  git+https://github.com/borisdayma/dalle-mini.git \
  git+https://github.com/patil-suraj/vqgan-jax.git

RUN pip install jupyter

WORKDIR /workspace

#Uses Fix Found Here: https://github.com/borisdayma/dalle-mini/issues/260
