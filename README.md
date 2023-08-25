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

2. **Phasors and ROIs Visualization:**
   - Visualize phasor shifts to offer an intuitive understanding of variations and trends within the data.
     
3. **Morphological Analysis and Clustering:**
   - Perform morphological analysis on the datasets, including clustering functionalities to group similar data points together.

4. **Statistical Analysis:**
   - Conduct statistical analysis on sample distributions, such as lifetime, G or S-wise properties. Provide insights into the underlying data characteristics.

5. **Detection of Coexisting Physical States:**
   - Identify molar fractions or intensity fractions of coexisting drugs' physical states within nano particles. Provide valuable insights into complex systems.

## Usage

Follow these steps to effectively use the features of this project in Google Colab:

### Dataset Creation
1. **Import Data:**
   - The code is designed to read data from `.R64` and `.ref` file formats.
   - Files need to be uploaded to the file section of Google Colab.
   - You have the option to either manually upload the files or simply drag and drop them into the file section.
   - The code will automatically process all uploaded files.
  
<img width="1421" alt="Screenshot 2023-08-25 at 15 27 28" src="https://github.com/Mariochem92/PhasorIdentifier/assets/51441240/5c2c55d4-268a-4473-b79c-fb87a9781906">

2. **File Formats:**
   - Supported formats: `.R64`, `.ref` and `.ifli` .
   - Please note that the `.ifli` format is not advised due to its large file size.
  
3. **Data Format and Structure:**
   - The uploaded `.R64` and `.ref` files should each contain the following arrays:
     - Intensity: Array representing the intensity values.
     - 1st Harmonic Phase: Array representing the phase values of the 1st harmonic.
     - 1st Harmonic Module: Array representing the module values of the 1st harmonic.
     - 2nd Harmonic Phase: Array representing the phase values of the 2nd harmonic.
     - 2nd Harmonic Module: Array representing the module values of the 2nd harmonic.
   - Ensure that the data arrays are properly aligned and correspond to each other.
   - If your data files do not match this structure, you might need to preprocess or reformat the data to fit the required arrangement.

4. **Pre-Processing Operations:**:
  - Make sure to compile all the necessary functions before proceeding with the main code execution.
  - Review and verify the input parameters that will be used in the main code section.
  - Ensure that the parameters are correctly set according to your specific use case and requirements.
   
<img width="1421" alt="Screenshot 2023-08-25 at 15 40 54" src="https://github.com/Mariochem92/PhasorIdentifier/assets/51441240/8930e634-a7a6-4813-9b28-a80e6e66e985">

### Input Parameters

Before running the code, make sure to set the following input parameters according to your specific needs:

1. **Threshold Selection:**
   - Set the thresholding method by commenting out the methods you're not using: Otsu, Multi-Otsu, or Custom.
   
2. **Extent of Median Filter:**
   - Adjust the extent of the median filter applied to the data. Alternatively, you can use a Gaussian filter.

3. **Frequency of FLIM Signal:**
   - Specify the frequency at which the FLIM signal was collected. The default is set to 80 MHz.

4. **Minimum Pixels for Phasor Detection:**
   - Set the minimum number of pixels required to detect the presence of a phasor.

5. **Minimum Pixels for ROI Detection:**
   - Specify the minimum number of pixels required to define the presence of a Region of Interest (ROI).

6. **ROI Contour Levels and Lower Frequency Levels:**
   - Define the number of contour levels used to detect an ROI (default: 8 levels).
   - Set the number of lower frequency levels to discard (default: 3 levels).

7. **Signal Percentile for Contour Upper Limit:**
   - Adjust the signal percentile used to set an upper boundary for the contour plot (default: 95th percentile).

8. **Type of Analysis:**
   - Choose the type of analysis: "Cumulative" or "Single File."
   - For cumulative analysis, the code uses the input file name.

By carefully configuring these input parameters, you can tailor the analysis to your data and research objectives. Make sure to review and adjust these settings before running the code for accurate and meaningful results.

  
<img width="1088" alt="Screenshot 2023-08-25 at 15 48 15" src="https://github.com/Mariochem92/PhasorIdentifier/assets/51441240/88133718-284f-4f24-b6ac-6dd29687bd70">

### Morphological Analysis and Clustering



