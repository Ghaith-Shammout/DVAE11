# A Comprehensive Evaluation Framework for Synthetic Time Series Data

## Project Structure

```
./  
|- config/              # Configuration files for each dataset (MUST be named <dataset-name>_config.yaml)
|- data/                # Contains the original dataset that needs to be processed
|- logs/                # Contains log files for system logging
|- outputs/             # Outputs from the pipelining process
|- scripts/             # Source code for the entire pipelining process
|- README.md            # Documentation file  
|- requirements.yaml    # Project dependencies
```


## Outputs Folder Structure

The `outputs` folder contains a subdirectory for each input dataset, named according to the dataset's name by convention. Each dataset-specific folder follows this structured format:

```
./  
|- data/              # Contains the preprocessed dataset along with its metadata file  
|- Evaluation/        # Contains subfolders for each population fidelity metric and F1 score per epoch. Additionally, this folder includes CSV files with aggregated metric results.  
|- models/            # Stores the trained synthesizer models for each epoch  
|- Plots/             # Includes visualizations for each metric  
|- Synth_Data/        # Contains generated data organized by epoch  
```

## Prerequisites

- Anaconda3 / Miniconda3

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```
2. Create the Conda environment:
   ```bash
   conda env create -f environment.yml
   ```
3. Activate the environment:
   ```bash
   conda activate main
   ```
4. Run the pipelining process:
   ```bash
   python scripts/pipeline.py
   ```

## GPU Utilization (Optional)

If you want to utilize a GPU for processing, ensure that CUDA is installed. The `environment.yaml` file should include the necessary dependencies for GPU acceleration.

To check GPU utilization, you can run:

```bash
nvidia-smi
```

This command will display GPU usage and resource allocation.

---


