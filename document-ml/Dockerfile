FROM jupyter/datascience-notebook:python-3.7.6

USER root

RUN apt-get update && \
    apt-get install -y tesseract-ocr libxml2-dev libxslt-dev rustc

RUN python3 -m pip install --no-cache-dir --upgrade pip && \
    python3 -m pip install --no-cache-dir \
    torch

RUN conda install -c huggingface transformers
    
RUN python3 -m pip install --no-cache-dir \
    scikit-learn \
    pytesseract \
    lxml \
    tensorboardx \
    seqeval \
    Pillow \
    pep517

RUN git clone https://github.com/microsoft/unilm.git
RUN cd unilm/layoutlm
RUN pip install unilm/layoutlm

WORKDIR '/home/jovyan/work/code/'