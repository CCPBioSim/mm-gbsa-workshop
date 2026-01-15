# CCPBioSim MM-GBSA Workshop

[![ci](https://github.com/ccpbiosim/mm-gbsa-workshop/actions/workflows/build.yaml/badge.svg?branch=main)](https://github.com/ccpbiosim/mm-gbsa-workshop/actions/workflows/build.yaml)
[![latest](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fccpbiosim.github.io%2Fworkshop.json&query=%24.containers.mm-gbsa-workshop.latest&labelColor=grey&logo=github&logoColor=white&label=latest&color=purple)](https://github.com/ccpbiosim/mm-gbsa-workshop/pkgs/container/mm-gbsa-workshop)
[![issues](https://img.shields.io/github/issues/ccpbiosim/mm-gbsa-workshop?logo=github&labelColor=grey)](https://github.com/CCPBioSim/mm-gbsa-workshop/issues)
[![pr](https://img.shields.io/github/issues-pr/ccpbiosim/mm-gbsa-workshop?logo=github&labelColor=grey)](https://github.com/CCPBioSim/mm-gbsa-workshop/pulls)

This workshop source repository contains the build recipe for a docker container derived from the CCPBioSim JupyterHub image. This container adds the necessary software packages and notebook content to form a deployable course container.

This workshop walks through the process of perfprming a basic MM-GBSA analysis of a molecular dynamics simulation of a protein-ligand complex to estimate the ligand binding free energy. The approach here uses *OpenMM* with a little help from *ParmEd*. 

This example uses data from a simulation performed using *OpenMM*, but could readily be adapted for use with simulations run with *Amber* or *GROMACS* (and maybe *CHARMM*).

![Figure 1](Figure1.png)

## How to Use

This training course is deployed on the [CCPBioSim](www.ccpbiosim.ac.uk) website via our cloud infrastructure, however you can deploy on your own machine with docker.

Pull the container from our repository::

    docker pull ghcr.io/ccpbiosim/mm-gbsa-workshop:latest

In our containers we are using the JupyterHub default port 8888, so you should
forward this port when deploying locally::

    docker run -p 8888:8888 ghcr.io/ccpbiosim/mm-gbsa-workshop:latest

## Authors

Workshop Content Authors:

- Charlie Laughton

## Contact

Please direct all questions and feedback to [Charlie Laughton](mailto:charles.laughton@nottingham.ac.uk)
