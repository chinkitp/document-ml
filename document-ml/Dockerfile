FROM jupyter/datascience-notebook:python-3.7.6

USER root

RUN apt-get update && \
    apt-get install -y tesseract-ocr

RUN python3 -m pip install --no-cache-dir --upgrade pip && \
    python3 -m pip install --no-cache-dir \
    torch \
    torchvision \
    scikit-learn \
    transformers[torch] \
    pytesseract

RUN apt-get install -y libxml2-dev libxslt-dev rustc

RUN git clone https://github.com/microsoft/unilm.git

WORKDIR '/home/jovyan/work/code/'