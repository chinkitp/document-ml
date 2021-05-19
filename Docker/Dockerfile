FROM jupyter/datascience-notebook

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

WORKDIR '/home/jovyan/work/code/'
