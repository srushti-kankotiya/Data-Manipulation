Excel Data Processing with Pandas
This Python script uses the pandas library to process Excel data from two sheets (fAST V1 and fAST V3) in the file fxyz-file.xlsx. It performs the following steps for each sheet:

Reads the Excel file into a dictionary of DataFrames.
Drops specific columns (asset_no in fAST V1 and asset_number in fAST V3).
Removes rows where certain columns (family_members and inpadoc_family_id in fAST V1, family_members and global_patent_family in fAST V3) are null.
Splits and explodes the values in the family_members column.
Removes duplicates based on the inpadoc_family_id column for fAST V1 and global_patent_family column for fAST V3.
Replaces specific characters in the family_members column of fAST V3.
Writes the processed data to a new Excel file final.xlsx, with each sheet containing the cleaned and processed data (fAST V1 and fAST V3).

Dependencies
Python 3.x
pandas library

How to Use

Install pandas if you haven't already:
pip install pandas

Run the script with Python:
python excel_data_processing.py

The processed data will be saved in final.xlsx with two sheets (fAST V1 and fAST V3).
