# Data-Fit-Model

## Description

Data-Fit-Model is a Python application designed to identify the best-fitting ideal functions for a given set of training data and map test points to these functions based on the least-square deviation criterion. The program processes datasets (training, ideal, and test), stores the results in an SQLite database, and visualizes the mappings and deviations using Bokeh.

## Table of Contents

- Installation
- Usage
- Features
- Project Structure
- Contributing

## Installation

1. To set up the project locally, follow these steps:

Clone the repository:

git clone https://github.com/Ahsan97Javed/Data-Fit-Model.git

2. Navigate to the project directory:

cd Data-Fit-Model

3. Install the required dependencies (Python and pip should be pre-installed):

pip install -r requirements.txt

## Usage

Prepare the Data: Ensure train.csv, ideal.csv, and test.csv are available in the project directory.

Run the Main Script:

python main.py

Output: The program will identify the ideal functions for each training function, map test points, calculate deviations, store results in ahsan.db, and generate interactive plots in the output directory.

## Features

### Data Processing and Mapping:

1. Selects the best-fit ideal functions from a set of 50 based on the training data.
2. Maps test points to ideal functions and computes the deviation based on specific criteria.

### Database Storage: Uses SQLite to store training data, ideal functions, and mapped test points with deviations.

### Data Visualization:

1. Generates interactive plots for ideal functions, training data, and test points using Bokeh.
2. Saves visualizations to HTML files in the output directory.

### Unit Tests: Includes tests for core functionality to ensure data processing accuracy and stability.
### Error Handling: Implements standard and user-defined exceptions to handle common errors.

## Project Structure
main.py: The main script for data processing, mapping, and visualization.
classes.py: Defines the primary classes:
SQLDataset: Handles loading CSV data into DataFrames and saving them to SQLite.
IdealFunction, IdealFunctionMapper, and IdealFunctionFinder: Classes for identifying and mapping ideal functions.
plotting.py: Contains the Plotter class, which uses Bokeh to generate interactive visualizations of data.
test.py: Includes unit tests to validate data processing and mapping functionalities.
ahsan.db: SQLite database storing processed data.
output/: Directory for generated HTML visualizations.
LICENSE: License file for the project.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.

2. Create a new branch for your feature or bug fix:

git checkout -b feature-name

3. Commit your changes:

git commit -m "Description of changes"

4. Push to the branch:

git push origin feature-name

5. Open a Pull Request and describe your changes.
