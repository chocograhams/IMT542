# IMT542-i4

## Overview
This repository contains Python code demonstrating how to access three different information structures using different access technologies, specifically tailored for use within Google Colab.

## How to Run in Google Colab:

1.  **Open in Colab:** Click on the `i4.ipynb` file to open it in Google Colab.

2. **Run Example 1 - CSV and Manual File Upload and Read Locally:**
    * Before running the first code cell, you need to upload a CSV file named `Repeat tags cleaned_SeaCoyottee - SME Highlights 2025-02-09 20_41` to your Colab environment.
    * Once the file is uploaded, run the cell by clicking its play button.
      
3.  **Run Example 2 - JSON and API Connection over HTTP:**
    * The second code cell will fetch data from a public JSON API and print a sample.
    * Simply run this cell by clicking the play button to its left. 

5.   **Run Example 3 - HTML and HTTP to Download Webpage:**
    * The third code cell will download the HTML content and print the title and the text of the first three paragraphs found on the webpage.
    * Simply run this cell by clicking the play button to its left. The `beautifulsoup4` library will be automatically installed by running the following command **before** running the HTML example function:
      ```python
      !pip install beautifulsoup4
      ```
      
The output of each successful data access will be printed below the respective code cell in your Colab notebook.


## Code Description:

The Python code in the Colab notebook defines three functions:

* `read_and_print_csv_from_uploaded_file(filename="sample.csv")`: Reads and prints a sample from a CSV file uploaded to Colab.
* `get_and_print_json_from_api()`: Fetches and prints data from a public JSON API.
* `get_and_print_multiple_paragraphs(url="https://www.example.com")`: Downloads the HTML content of a webpage and extracts and prints its title and the text of the first three paragraph elements.
