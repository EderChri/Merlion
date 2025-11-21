FROM python:3.9-slim-bullseye
WORKDIR /opt/Merlion
# Install Java
RUN rm -rf /var/lib/apt/lists/* && \
    apt-get clean && \
    apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y --no-install-recommends openjdk-11-jre-headless && \
    rm -rf /var/lib/apt/lists/*
# Install Merlion from source
COPY *.md ./
COPY setup.py ./
COPY merlion merlion
RUN pip install "./"
