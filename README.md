# Fuzzy Logic Workshop Recommendation System

This project implements a fuzzy logic-based recommendation system designed to rank workshops based on service quality and price. The system evaluates inputs using fuzzification, applies inference rules, and produces a ranked output with defuzzified scores. The implementation is provided in a **Jupyter Notebook (`.ipynb`)** format.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Fuzzy Logic Process](#fuzzy-logic-process)
3. [Features](#features)
4. [How to Use](#how-to-use)
5. [Dependencies](#dependencies)
6. [Acknowledgments](#acknowledgments)

---

## Project Overview

This system provides a ranking of workshops based on two key factors:

1. **Service Quality**: Rated on a scale of 0–100.
2. **Price**: Rated on a scale of 0–10.

Using fuzzy logic, the system converts these numerical scores into linguistic variables (e.g., "good," "fair," "cheap") and evaluates them using predefined rules. The output is a ranked list of workshops, with higher scores indicating better recommendations.

---

## Fuzzy Logic Process

### 1. **Fuzzification**
   - Converts numerical scores into linguistic terms with membership values:
     - Service Quality: "buruk" (bad), "cukup" (fair), "bagus" (good).
     - Price: "murah" (cheap), "mahal" (expensive).

### 2. **Inference**
   - Applies rules to determine the recommendation level:
     - If service is "buruk," the workshop is "not recommended."
     - If service is "cukup," it is "recommended" only if the price is "murah."
     - If service is "bagus," it is always "recommended."

### 3. **Defuzzification**
   - Converts fuzzy outputs into crisp scores for ranking.

### 4. **Ranking**
   - Sorts workshops based on defuzzified scores and assigns ranks.

---

## Features

- **Dynamic Input Handling**: Processes workshop data from an Excel file.
- **Comprehensive Ranking**: Produces a ranked list of workshops based on service quality and price.
- **Top 10 Results Export**: Outputs the top 10 recommendations to an Excel file for easy sharing and analysis.

---

## How to Use

### **1. Using in Google Colab**
   - Open the notebook in Google Colab.
   - Upload the `bengkel.xlsx` file before running the program:
     1. Click the folder icon on the left sidebar.
     2. Use the upload button to upload the file.
   - Execute the notebook cells step by step to generate the results.

### **2. Running Locally Using Visual Studio Code**
   - Install **Visual Studio Code** and the **Python Extension** from the Extensions Marketplace.
   - Install **Jupyter** support for VS Code:
     1. Open VS Code.
     2. Go to the Extensions Marketplace and search for `Jupyter`.
     3. Install the extension.
   - Ensure Python and the required libraries are installed (see [Dependencies](#dependencies)).
   - Place the `bengkel.xlsx` file in the same directory as the notebook file.
   - Open the `.ipynb` file in VS Code.
   - Click "Run All" or execute the cells sequentially to process the data and save the output to `peringkat.xlsx`.

---

## Dependencies

This project requires the following Python libraries:

- **pandas**: For data manipulation and Excel file handling.
- **openpyxl**: For reading and writing Excel files.
- **Jupyter**: For running `.ipynb` notebooks.

Install dependencies using pip:
```bash
pip install pandas openpyxl notebook
```

---

## Acknowledgments

This project was developed as part of the Artificial Intelligence Introduction course by:

- **Filza Rahma Muflihah (1301201261)**  
- **Ummu Husnul Khatimah (1301204120)**  

We would like to thank the course instructors for their guidance and support in the completion of this project.

If you find this notebook helpful, feel free to use it for your studies or projects. Feedback and contributions are welcome!