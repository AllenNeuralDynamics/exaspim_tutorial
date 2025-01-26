# hash:sha256:8985636fc2f399ba7ad3a115e3ee41f7fa0a056f6ccf9e78c54c4ab8a765678b
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/jupyterlab:3.0.9-miniconda4.9.2-python3.8-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN pip install -U --no-cache-dir \
    cloud-volume==10.2.2 \
    ipywidgets==8.1.3 \
    k3d==2.16.1 \
    matplotlib==3.9.0 \
    numpy==1.26.4 \
    pandas==2.2.2 \
    skeleton-plot==0.0.10

COPY postInstall /
RUN /postInstall
