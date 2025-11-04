# Start with BioSim base image.
ARG BASE_IMAGE=latest
FROM ghcr.io/ccpbiosim/jupyterhub-base:$BASE_IMAGE

LABEL maintainer="James Gebbie-Rayet <james.gebbie@stfc.ac.uk>"

# Switch to jovyan user.
USER $NB_USER
WORKDIR $HOME

# Install workshop deps
RUN mamba install parmed mdtraj openmm matplotlib -y

# Get workshop files and move them to jovyan directory.
COPY --chown=1000:100 . .
RUN rm -rf environment.yaml Figure1.png Figure1.pptx INSTALL.txt LICENSE micromamba README.md run_notebook.sh docker .git .github

# Copy lab workspace
#COPY --chown=1000:100 docker/default-37a8.jupyterlab-workspace /home/jovyan/.jupyter/lab/workspaces/default-37a8.jupyterlab-workspace

# Always finish with non-root user as a precaution.
USER $NB_USER
