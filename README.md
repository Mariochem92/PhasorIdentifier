# PhasorIdentifier
Analyze FLIM files (.R64, .ref) effortlessly in Google Colab. Masking, cell segmentation, pH correlation, nanoscale effects, and precise quantification. Versatile for various research scenarios.


[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.8282839.svg)](https://doi.org/10.5281/zenodo.8282839)

[![Version](https://img.shields.io/badge/Version-1.0.0-blue)](https://your-repo-url)

[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightred)](https://creativecommons.org/licenses/by-nc/4.0/legalcode)

## Notebook Setup

To begin using this project, follow these steps to run the code in Google Colab. Running the notebook in Google Colab is recommended as it provides access to powerful GPUs and eliminates concerns related to memory and disk space.

1. **Download the Notebook:**
   - Click on the notebook file in the repository (typically ending with `.ipynb` extension).
   - In the GitHub interface, you can click the "Download" button to save the notebook to your computer.

2. **Save the Notebook to Google Drive:**
   - Open your Google Drive account.
   - Create a new folder or use an existing one to organize your Colab notebooks.
   - Upload the downloaded notebook to the selected folder.

3. **Open the Notebook in Google Colab:**
   - Right-click on the uploaded notebook in Google Drive.
   - Choose "Open with" and select "Google Colaboratory."

4. **Run the Notebook:**
   - Once the notebook is open in Google Colab, you can run each code cell by clicking the "Play" button or using the keyboard shortcut Shift + Enter.
   - Follow the instructions provided within the notebook for each section.

**Note for Local Execution:**
If you prefer to run the notebook locally, keep in mind the following considerations:
- Make sure the file import paths are correctly set to reflect your local directory structure.
- You might need to have Python and required dependencies installed locally.
- For optimal performance, using Google Colab is recommended due to its access to GPU resources and ease of use.

## Features

1. **Dataset Creation:**
   - Generate two datasets: one for collecting identified phasors and another containing detailed information about each data point imported from files.

2. **Morphological Analysis and Clustering:**
   - Perform morphological analysis on the datasets, including clustering functionalities to group similar data points together.

3. **Statistical Analysis:**
   - Conduct statistical analysis on sample distributions, such as lifetime, G or S-wise properties. Provide insights into the underlying data characteristics.

4. **Phasor Shifts Visualization:**
   - Visualize phasor shifts to offer an intuitive understanding of variations and trends within the data.

5. **Detection of Coexisting Physical States:**
   - Identify molar fractions or intensity fractions of coexisting physical states within nano particles. Provide valuable insights into complex systems.




