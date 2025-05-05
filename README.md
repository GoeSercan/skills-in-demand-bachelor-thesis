# Skills in Demand – Bachelor Thesis (2025)

This repository contains the full workflow including scripts, and node descriptions for a Bachelor thesis focused on the extraction of skills from AI/ML-related job advertisements using KNIME.

## Project Overview

- **Thesis Title:** _"Skills in Demand for AI and ML Roles: A comparative study of Job Postings across English- and German-Speaking Countries"_
- **Platform:** KNIME Analytics Platform
- **Main Goal:** Extract and analyze the demand for skills from AI/ML-related job postings across countries using structured workflows and hybrid extraction techniques.

## How to Use the KNIME Workflow

### Prerequisites
- **KNIME Analytics Platform** (Version ≥ 5.4.0 recommended)
- Python ≥ 3.9.20 (for script nodes)
- Installed Python packages:
  - `pandas`
  - `torch`
  - `transformers`
  - `rapidfuzz`

### Step-by-Step Instructions

1. **Download the Repository or Files**
   - Clone/download this GitHub repo or the files within to your local machine.

2. **Open KNIME** 
   - Open the `skills-in-demand-bachelor-thesis.knwf` workflow from the `knime-workflow` folder inside of KNIME.

3. **Set the Files for the File Reader Nodes (Required):**
   - The workflow expects the following files to be present:
     - `job-data/Sample_Data_2000_Job_Entries.csv` (or the full dataset, which will be linked below)
     - `country_code_mappings/Country_Code_Mappings.csv`
     - `skill-base/Skills_List.csv`

4. **Optional: Full Dataset**
   - The full unzipped dataset (~5.5 GB, multilingual) can be downloaded via Dropbox:
     [Download Full Dataset (.zip)](https://www.dropbox.com/scl/fi/zmosdbmycpvosrmcdnejm/All_Job_Entries.csv.zip?rlkey=8axtyzwjv0pq28f9db89g7ljq&st=rafjr5ju&dl=0)
   - Unzip the file and replace `Sample_Data_2000_Job_Entries.csv` with `All_Job_Entries.csv` in the first File Reader node.

5. **Run the Workflow**
   - Execute each node separately or use the **"Execute All"** option.
   - The pipeline consists of:
     - Data Cleaning & Filtering
     - Location Parsing & Normalization
     - Title Filtering and Description Cleaning
     - Skill Extraction
     - Visualizations

