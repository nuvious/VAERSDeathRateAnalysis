- [Overview](#overview)
  - [TLDR](#tldr)
  - [Running the Notebook](#running-the-notebook)
    - [Download the entire VAERS dataset:](#download-the-entire-vaers-dataset)
    - [Run Analysis](#run-analysis)
  - [References](#references)

# Overview

This is a simple jupyter noteboook to analyze the VAERS dataset specifically to analyze the relationship to reported deaths against baseline pre-COVID age adjusted death rate.

## TLDR

As of 9/28/2021 when this notebook was authored and the VAERS dataset downloaded, the following were the analysis results:

```
Of the 184285800 fully vaccinated americans, 24580 deaths were reported in VAERS.

This yields a 13.34 deaths per 100k for fully vaccinated individuals in the US.

To compare the age-adjusted mortality rate in 2018 (before COVID) in the US was 723.6 per 100k which is 54.24 times higher than the VAERS reported COVID19 death rate.
```

Overall the VAERS dataset, despite containing entries for deaths do not on their own provide substantial causal evidence for death and the COVID 19 vaccines available to the public. Deaths reported in realtion to the COVID vaccine in VAERS fall so far below the pre-COVID death rate any assumption of causal link need substantially better evidence than the death entries in VAERS.

This further support the caution in the VAERS user guide that:

"...the inclusion of events in VAERS data does not 
infer causality." - (Food and Drug Administration, 2020)

If you're reading this and aren't vaccinated and have been compelled by arguments related to VAERS in the past, please reconsider.

## Running the Notebook

### Download the entire VAERS dataset:
 - Go to [https://vaers.hhs.gov/data/datasets.html](https://vaers.hhs.gov/data/datasets.html).
 - Choose the "All Years Data" option.

   ![](doc\vaers_screenshot.png)
 - Enter the CAPTCHA and begin the download.
 - Copy the AllVAERSDataCSVS.zip file to the same directory as the notebook and unzip to the AllVAERSDataCSVS directory.

### Run Analysis

 - **OPTIONAL** - Create a vritual environment
```bash
# Linux
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
./venv/Scripts/activate.ps1
```
 - Install requirements.
```bash
# Linux 
pip3 install -r requirements.txt

# Windows
pip install -r requirements.txt
```
 - Run jupyter lab.
 ```bash
# Linux
python3 -m jupyterlab

# Windows
python -m jupyterlab
 ```
  - Update top-most cell in the notebook for current percentage of US population that is fully vaccinated.

![](doc\top_cell.png)
  - In the menu run Kernel > Restart Kernel and Run All Cells

## References

Food and Drug Administration. (2020). VAERS DATA USE GUIDE Contents. Retrieved from https://vaers.hhs.gov/docs/VAERSDataUseGuide_November2020.pdf
