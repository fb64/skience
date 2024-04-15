
FROM jupyter/base-notebook

USER root

# Install java 17
RUN apt-get update \
    && echo "Updated apt-get" \
    && apt-get install -y openjdk-17-jre \
    && echo "Installed openjdk 17"

# Install kotlin kernel for jupyter using conda
RUN conda install -y -c jetbrains kotlin-jupyter-kernel && echo "Kotlin Jupyter kernel installed via conda"

# Let's change to  "$NB_USER" command so the image runs as a non root user by default
USER ${NB_UID}

#Enable jupyter lab
ENV JUPYTER_ENABLE_LAB=yes