This file provides the documentation for two web scraping scripts that aim to retrieve financial reports from online sources. 


# Configuration/Installation

Anaconda is a distribution of the Python and R programming languages for scientific computing (data science, machine learning applications, large-scale data processing, predictive analytics, etc.), that aims to simplify package management and deployment. It includes an installation of Jupyter Notebook, which presents data science documents that combine live-code with narrative text, equations and visualizations. 

The web scraping code is written in Python. The latest version of Python should be installed. Various Python packages and libraries are required for web scraping, and must be installed before using this code. 

# files included

## microsoft.ipynb
File for scraping Microsoft financial data.

## Microsoft.xlsx
Accompanying file with initial data that is used to create the CSV file.

## sony.ipynb
File for downloading Sony financial data.


# Microsoft

This file scrapes financial information from Microsoft Investor Relations (www.microsoft.com/en-us/Investor). Microsoft reports segment revenues by fiscal year quarter. The Jupyter Notebook file extracts quarterly segment revenues and operating expenses for a particular quarter of a fiscal year. The figures are saved to a .csv file, which can be loaded into R.

## Required Packages/Libraries

Requests is a library that will allow us to send HTTP requests to get HTML files. From Requests, the GET method indicates that you’re trying to get or retrieve data from a specified resource. To make a GET request, invoke requests.get()

BeautifulSoup is a Python library for pulling data out of HTML and XML files. This will help us parse the HTML files.

pandas is a Python data analysis library, which will help us assemble the data into a DataFrame to clean and analyze it

NumPy is a Python library used for working with large, multi-dimensional arrays and matrices. It will add support for mathematical functions and tools for working with arrays.

The time module in Python has a function sleep() that you can use to suspend execution of the calling thread 

The randint() method returns a pseudo-random integer number 

## Operating Instructions

To open the file, navigate to the directory in Jupyter Notebook and click on the filename. A single block of code can be run by selecting the block and clicking "Run" at the top of the Jupyter Notebook interface. This will only run the selected block. Separate blocks correspond to separate actions the code can undertake.

Using this code, you can scrape data from a range of quarters or a single quarter by altering the specified reference dates. When first creating the CSV file, run the first, second and third code blocks. When future data becomes available, you can add to the CSV file by running the first, second, and fourth code blocks. 

# Sony

This file downloads PDF files from Sony Investor Relations (https://www.sony.com/en/SonyInfo/IR/library/presen/er/archive.html) into a specified directory. Sony does not provide the required financial information in HTML format, but downloading the PDF files through the code instead of manually downloading should be a time-saving process. The code also converts the downloaded files to HTML, but these conversions are difficult to scrape using BeautifulSoup due to the formatting of PDFs and the lack of distinction between relevant and irrelevant tables. Nevertheless, they may provide useful information in the future

## Required Packages/Libraries

the O/S module provides a portable way of using operating system dependent functionality. 

NumPy is a Python library used for working with large, multi-dimensional arrays and matrices. It will add support for mathematical functions and tools for working with arrays.

wget is a module used to download files

PDFMiner is a text extraction tool for PDF documents that obtains the exact location of text as well as other layout information (fonts, etc.), performs automatic layout analysis, and can convert PDF into other formats (HTML/XML).

## Operating Instructions

To open the file, navigate to the directory in Jupyter Notebook and click on the filename. A single block of code can be run by selecting the block and clicking "Run" at the top of the Jupyter Notebook interface. 
