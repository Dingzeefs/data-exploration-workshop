# Data Exploration Workshop - Collaboration

This repository contains the code and data for the "Collaboration" workshop that is part of the Data Exploration semester of the Master of Applied Data Science at HAN University of Applied Sciences.

## Project Overview

This project explores a dataset containing a target variable and 100 feature variables. The goal is to identify the most relevant features through correlation analysis and create a processed dataset with only the most useful features.

## Directory Structure

- `data/raw/`: Contains the original dataset (`correlation_jngdc.csv`)
- `data/processed/`: Will contain the processed dataset with selected features
- `exploration_[name].ipynb`: Jupyter notebook with the data exploration process

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- uv (Python package manager)

### Installation

1. Clone this repository:
   ```
   git clone [repository-url]
   cd [repository-name]
   ```

2. Create and activate a virtual environment:
   ```
   uv venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. Install the required packages:
   ```
   uv pip sync requirements.txt
   ```

### Dependency Management

This project uses UV for dependency management with the following files:

- `requirements.in`: Contains the high-level dependencies without version constraints
- `requirements.txt`: Contains the locked dependencies with exact versions, generated from requirements.in

To update the locked dependencies:
```
uv pip compile requirements.in --output-file requirements.txt
```

To add a new dependency:
1. Add it to `requirements.in`
2. Run `uv pip compile requirements.in --output-file requirements.txt`
3. Run `uv pip sync requirements.txt`

### Running the Notebook

You can run the Jupyter notebook in one of two ways:

#### Option 1: Using uv

```
uv run --with jupyter jupyter lab
```

#### Option 2: Using VSCode

1. Open the project folder in VSCode
2. Select the Python interpreter from the virtual environment (.venv)
3. Open the notebook file and run it using VSCode's built-in Jupyter support

## Data Analysis Process

1. Load the raw data from `data/raw/correlation_jngdc.csv`
2. Explore the dataset structure and calculate correlations
3. Identify the most relevant features based on correlation with the target variable
4. Create a processed dataset with only the selected features
5. Save the processed dataset to `data/processed/`

## Collaboration

This project is designed for collaboration. Partners can:
1. Fork or clone the repository
2. Create their own exploration notebooks
3. Commit and push changes
4. Merge findings into a final notebook 