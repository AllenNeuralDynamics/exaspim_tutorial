# hash:sha256:e88fae45389feed8901673adfccb4825abb62a48505e89bf35ea43e28da9f573
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/py-r:python3.10.12-R4.2.3-IRkernel-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN pip install -U --no-cache-dir \
    cloud-volume==10.2.2 \
    ipywidgets==8.1.3 \
    k3d==2.16.1 \
    matplotlib==3.10.0 \
    numpy==1.26.4 \
    pandas==2.2.3 \
    skeleton-plot==0.0.10

COPY postInstall /
RUN /postInstall
