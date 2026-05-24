# Movie Data Scraper (IMDb & Wikipedia)

This project is a Python-based data pipeline that integrates movie details from IMDb and Wikipedia. 
It combines local big-data processing with real-time API calls to build a comprehensive movie dataset.

## Data Sources & Setup

### 1. IMDb Datasets
Download the following files from the official IMDb repository: [https://datasets.imdbws.com/](https://datasets.imdbws.com/)

**Required Files:**
* `title.basics.tsv.gz`: Core information.
* `title.ratings.tsv.gz`: Audience ratings and vote counts.
* `title.principals.tsv.gz`: Cast and crew information.

**⚠️ Important - Configuration:**
Before running the script, you **must update the file paths** in the code to match the location where you saved these files on your computer. Look for the path variables at the beginning of the script and update them accordingly.

### 2. Performance & Storage
* **Do NOT extract the files**: The script is optimized to read `.tsv.gz` files directly to save disk space and prevent system crashes.
* **Memory Management**: The `title.principals` file is very large. It is recommended to close heavy background applications (like Chrome) during execution to ensure enough RAM is available.

## Installation

Ensure you have Python 3.x installed. Install the necessary libraries using the following command:

```bash
pip install requests beautifulsoup4 pandas numpy


