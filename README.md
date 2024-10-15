# CHORDS Data Downloader

This Python script automates the process of downloading data from the CHORDS database using its API, and saves the data as a CSV. The script is configurable for different CHORDS portals and user-defined parameters.

## Features
- Retrieves data from the CHORDS database
- Supports customizable API parameters
  - CHORDS portal, instrument ID's, data period in addition to other optional parameters
- Saves the downloaded data as a CSV, with variable (sensor) shortnames used as column headers
- Includes API error handling, including an exponential backoff method to reduce excess datapoints

## Requirements

To run this script, you’ll need:
- Python 3.11.6+
- The following Python libraries:
  - `requests` for making API requests
  - `pandas` 
  - `json`
  - `numpy`
  - `datetime`

Install the required libraries with:

```bash
pip install requests pandas