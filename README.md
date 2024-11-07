# CHORDS Data Downloader

This Python script automates the process of downloading data from the CHORDS database using its API and saves the data as a CSV. The script is configurable for different CHORDS portals and user-defined parameters.

## Features
- Retrieves data from the CHORDS database
- Supports customizable API parameters
  - CHORDS portal, instrument ID's, and data period in addition to other optional parameters
- Saves the downloaded data as a CSV, with variable (sensor) shortnames used as column headers
- Includes API error handling, most noteably an exponential backoff method to reduce excess datapoints

## Requirements

To run this script, you’ll need:
- Python 3.6 or higher
- The following Python libraries:
  - `requests` for making API requests
  - `pandas` for CSV creation
  - `json` for API data retrieval
  - `numpy` 

Install the required libraries with:

```bash
pip install requests pandas numpy 
```

## Documentation
In-depth documentation may be found at: https://docs.google.com/document/d/1qqs5X0vSslAEYBxlAh95oDgC1dG5xmBKVknz7wl1QxA/edit?usp=sharing

## Usage
To use this script, simply modify the user parameters to your specifications.
Below are the parameters you will interact with. 

REQUIRED: portal_url, portal_name, data_path, instrument_IDs, user_email, api_key, start, end

```python
fill_empty = '' # OPTIONAL
include_test = False # OPTIONAL

portal_url = r"https://chords.portal.com/"
portal_name = "PORTAL NAME"
data_path = r"C://path//to//local//storage//" 
instrument_IDs = [
    1,2,3
]
user_email = ''
api_key = '' 
start = 'YYYY-MM-DD HH:MM:SS'
end = 'YYYY-MM-DD HH:MM:SS'

columns_desired = [] # OPTIONAL             it is important that the list be empty if no columns are to be specified!
time_window_start = 'HH:MM:SS' # OPTIONAL   it is important that these be empty strings if no time window is to be specified!
time_window_end = 'HH:MM:SS' # OPTIONAL
```
