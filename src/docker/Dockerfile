
FROM quay.io/jupyter/base-notebook

USER root

# Install java 21
RUN apt-get update && apt-get install -y openjdk-21-jre && apt-get clean

# Install kotlin kernel for jupyter using conda
RUN pip install kotlin-jupyter-kernel

# Let's change to  "$NB_USER" command so the image runs as a non root user by default
USER ${NB_UID}

#Enable jupyter lab
ENV JUPYTER_ENABLE_LAB=yes