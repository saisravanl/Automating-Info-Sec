# Log Frequency by Name Script

## Overview

This script processes a log file in CSV format, extracts timestamp information, and generates a frequency table of log entries grouped by month. The results are then plotted using Matplotlib.

## Prerequisites

- Python 3.x
- pandas
- matplotlib

Ensure that the required Python packages are installed. You can install them using pip:

```bash
pip install pandas matplotlib
```

## Usage

To run the script, use the following command:

```bash
python logfreqbyname.py <path_to_log_file>
```

### Arguments

- `<path_to_log_file>`: The path to the CSV log file you want to process.

## Example

```bash
python logfreqbyname.py logs.csv
```

### Output

The script will print the column names of the log file, show the first five rows of the extracted timestamps, and convert the `TimeGenerated` column to a DateTime dtype. It will then generate and display a plot of the frequency of log entries grouped by month.

## Script Details

1. **File Validation**: The script first checks if the provided file exists and is readable.
2. **Data Loading**: It loads the CSV file into a pandas DataFrame, skipping the first row.
3. **Column Display**: It prints the column names of the DataFrame.
4. **Timestamp Extraction**: Extracts the `TimeGenerated` and `TimeWritten` columns and displays the first five rows.
5. **Timestamp Conversion**: Converts the `TimeGenerated` column to DateTime dtype.
6. **Frequency Table**: Groups the log entries by month based on the `TimeGenerated` column and counts the entries.
7. **Plotting**: Plots the frequency table.

## Notes

- The script expects the log file to have columns named `TimeGenerated` and `TimeWritten`.
- The encoding for reading the CSV file is set to `ISO-8859-1`.
- The script uses an interactive Matplotlib mode for plotting.
