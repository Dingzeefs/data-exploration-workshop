# README

This repository contains a notebook and data for the workshop "Collaboration" that is part of the Data Exploration semester of the Master of Applied Data Science at HAN University of Applied Sciences.

## Lesson goal

The student performs an exploration of a given data set and shares the process and results in such a way that they can be reproduced.

## Files

- This file :-)
- A .gitignore file you can use in your own repositories (see below).
- `data/raw/correlation_jngdc.csv` : the data file you will be using as source data.

## Preparation

1. Install uv and create a new project containing jupyter, pandas, numpy, scikit-learn, statsmodels, matplotlib and seaborn:

`uv add pandas numpy matplotlib seaborn scikit-learn statsmodels ipykernel`. 

2. Before you make your first commit ensure you have a .gitignore file that prevents virtual environments and other files that are for local use only to be added to git. Copying the .gitignore file from the repository you're reading now is fine.

3. Set up your project:
   1. Create a directory "data" and below that two subdirectories "raw" and "processed". Remember that git does not store empty directories. Create empty .gitkeep files to work around this.
   2. Download the file `data/raw/correlation_jngdc.csv` from the repository you're reading now to your own `data/raw/` directory.
   3. Create a new notebook `exploration_[your_name_without_spaces].ipynb`.
4. Create a REAME.md file. Use it to explain what a user needs to do to run your project. At the very least explain how to start the notebook server (either with `uv run --with jupyter jupyter lab` or by opening the project folder in VSCode).
5. Commit your project to a public repository on GitHub.

## Useful Pandas commands you may not have seen before

- To calculate correlations: `df.corr`
- To create a new column with absolute values based on another column: `df['abs'] = df['col'].abs()` (remember that correlations can be both positive and negative!).
- To drop a row based on a specific index value: `df.drop(labels='index_to_drop', axis='index)`.
- To show the rows with the n highest values in a column: `df.nlargest(n, 'col')`.

## The workshop

1. Make sure you've done all the steps listen under "Preparation" above.
2. Open your notebook `exploration_[your_name_without_spaces].ipynb` and use it to explore the data set `data/raw/correlation_jngdc.csv` using the techniques you have learned so far and the techniques listed under "Useful Pandas commands you may not have seen before" above. This data set contains a single target variable (helpfully named "target") and 100 feature variables. Make sure your notebook provides information about the dataset that is useful to others that need to work with this file. 
3. Turn the source data into a new data file that contains only the target variable and a few of the feature variables that are useful (at least 5). Save this data file in `data/processed`.
4. Push your work to your repo. This repo should be public. 
5. Exchange repos with one of your classmates. Divide the variables among the two of you. Each of you will perform a further exploration of the assigned variables and note the results in a notebook. Make sure each of you uses their own notebook to avoid merge conflicts.
6. When you're both done, commit your work and push it (you will need to give your partner permissions to your repository on GitHub).
7. Create a new notebook that contains all your work in one notebook.

