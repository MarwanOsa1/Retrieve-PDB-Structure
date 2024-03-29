# Retrieve-PDB-Structure
Importing libraries: This section imports the necessary libraries for the code execution, including RCSB Search API, Bio.PDB, os, and pandas.

1-Search process simulation: This section defines several queries to simulate the search process. It creates TextQuery and AttributeQuery objects to specify search conditions such as the presence of a transcription factor, the experimental method being X-ray diffraction, resolution not exceeding 3.0, containing the phrase "sodium" in the chemical compound name, and originating from the species Homo sapiens. The queries are combined and executed, and the number of matching structures is printed.

2-Downloading mmCIF files: This section uses the PDBList class from Bio.PDB to download the mmCIF files for each protein structure that matched the search criteria. The code is currently commented out, but it would iterate over the query results and retrieve the files using the PDB IDs.

3-Extracting data from mmCIF files: This section defines a list of specific data fields needed from the mmCIF files. It creates a dictionary to store the extracted data. It then iterates over the mmCIF files in the "data" directory and converts each file to a dictionary using the MMCIF2Dict function from Bio.PDB, and extracts the desired data fields. If a field is missing in a file, it is assigned the value "N/A".

4-Storing data in an Excel file: This section creates a pandas DataFrame from the extracted data dictionary. It specifies the path and name for the Excel file as "output.xlsx" and saves the DataFrame to that file using the to_excel method.

5-Printing the Excel file path: The path of the generated Excel file is printed to the console.

#improvements can be made to the code:
#  1-make a new input to take the user search criteria
#  2- make the user choose the number of downloads
#  3-make the user input the path where he wants the CIF files to be downloaded
#  4-make the user choose the data needed from the CIF file 
#  5-make the user choose the Excel file name and its location

#if you would like to know more about the code and how to customize your RCSB search, contact:marwanosama3002@gmail.com
#©2024 Marwan Osama.All rights reserved
