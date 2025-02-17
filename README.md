# Template for developing Snakemake workflows

Brief description of workflow

## Required input data

Add info here

## Produced output data

Add info here

# Deploying the workflow on execution hardware

1. run `./init.py` (requires Python3)
    - this will create an "execution" Conda environment,
    and a Snakemake working directory plus standard subfolders
    one level above the repository location
2. activate the created Conda environment: `cd .. && conda activate ./exec_env`
3. prepare profile and configuration files as necessary, and run Snakemake


# Developing the workflow locally

1. run `./init.py --dev-only` (requires Python3)
  - this will skip creating the workflow working directory and subfolders
2. activate the created Conda environment: `conda activate ./dev_env`
3. write your code
4. run the recommended code checks with the following tools:
    - Python scripts:
        - linting: `pylint <script.py>`
        - organize imports: `isort <script.py>`
        - code formatting: `black [--check] .`
    - Snakemake files:
        - linting: `snakemake --lint`
        - code formatting: `snakefmt [--check] .`
5. after checking and standardizing your code, commit your changes:
