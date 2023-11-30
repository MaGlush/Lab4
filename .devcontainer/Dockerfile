FROM --platform=linux/amd64 ubuntu:latest

USER root

RUN apt-get update && apt-get install -y git curl
RUN curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-$(uname)-$(uname -m).sh
RUN bash Mambaforge-$(uname)-$(uname -m).sh -b
ENV PATH=/root/mambaforge/bin:$PATH
RUN mamba create -n isl_sage sage python=3.11 pycryptodome numpy pandas -y -vv
RUN mamba init bash
