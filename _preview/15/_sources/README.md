<img src="notebooks/images/logos/NCAR-contemp-logo-blue.svg" alt="NCAR logo" width="500"/>

# CESM LENS on AWS Cookbook

[![nightly-build](https://github.com/ProjectPythia/cesm-lens-aws-cookbook/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/cesm-lens-aws-cookbook/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/cesm-lens-aws-cookbook/main?labpath=notebooks)

This Project Pythia Cookbook covers analysis of CESM LENS data publicly available on Amazon S3 (us-west-2 region) using Xarray and Dask

## Motivation

The [National Center for Atmospheric Research (NCAR)](https://ncar.ucar.edu/) Community Earth System Model Large Ensemble ([CESM LENS](https://www.cesm.ucar.edu/community-projects/lens)) dataset includes a 40-member ensemble of climate simulations for the period 1920-2100. All model runs were subject to the same radiative forcing scenario: historical up to 2005, and RCP8.5 thereafter. RCP8.5 - Representative Concentration Pathway 8.5 - refers to the worst-case scenario considered in the [Fifth Assessment Report of the Intergovernmental Panel on Climate Change (IPCC AR5)](https://www.ipcc.ch/report/ar5/wg1/). Each of the 40 runs begins from a slightly different initial atmospheric state (created by randomly perturbing temperatures at the level of round-off error). The data comprise both surface (2D) and volumetric (3D) variables in the atmosphere, ocean, land, and ice domains.

The total LENS data volume is ~500 TB, and is traditionally accessible through the NCAR Climate Data Gateway ([CDG](https://www.earthsystemgrid.org/dataset/ucar.cgd.ccsm4.CESM_CAM5_BGC_LE.html)) for download or via web services. A subset (currently ~70 TB compressed) including the most useful variables is now [freely available on AWS S3](https://registry.opendata.aws/ncar-cesm-lens/) thanks to the [AWS Public Dataset Program](https://aws.amazon.com/opendata/open-data-sponsorship-program/).

## Authors

[See contributors to the `NCAR/cesm-lens-aws` repository](https://github.com/NCAR/cesm-lens-aws/graphs/contributors)

### Contributors

<a href="https://github.com/ProjectPythia/cesm-lens-aws-cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/cesm-lens-aws-cookbook" />
</a>

## Structure

### Foundations
There is one notebook in this section that describes how to access the CESM LENS data from AWS using Intake ESM. It includes examples of using an enhanced catalog.

### Example workflows
This section contains an example of using this dataset to recreate two plots from a paper published in BAMS.

## Running the Notebooks
You can either run the notebook using [Binder](https://binder.projectpythia.org) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org), which enables the execution of a
[Jupyter Book](https://jupyterbook.org) in the cloud. The details of how this works are not
important for now. All you need to know is how to launch a Pythia
Cookbooks chapter via Binder. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon, (see figure below), and be sure to select
“launch Binder”. After a moment you should be presented with a
notebook that you can interact with. I.e. you’ll be able to execute
and even change the example programs. You’ll see that the code cells
have no output at first, until you execute them by pressing
{kbd}`Shift`\+{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter.html).

### Running on Your Own Machine
If you are interested in running this material locally on your computer, you will need to follow this workflow:

(Replace "cookbook-example" with the title of your cookbooks)   

1. Clone the `https://github.com/ProjectPythia/cesm-lens-aws-cookbook` repository:

   ```bash
    git clone https://github.com/ProjectPythia/cesm-lens-aws-cookbook.git
    ```  
1. Move into the `cesm-lens-aws-cookbook` directory
    ```bash
    cd cesm-lens-aws-cookbook
    ```  
1. Create and activate your conda environment from the `environment.yml` file
    ```bash
    conda env create -f environment.yml
    conda activate cla-cookbook-dev
    ```  
1.  Move into the `notebooks` directory and start up Jupyterlab
    ```bash
    cd notebooks/
    jupyter lab
    ```
