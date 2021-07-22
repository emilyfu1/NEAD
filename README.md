This file provides the documentation for two web scraping scripts that aim to retrieve financial reports from online sources. 


# Installation and Setup

Anaconda is a distribution of the Python and R programming languages for scientific computing (data science, machine learning applications, large-scale data processing, predictive analytics, etc.), that aims to simplify package management and deployment. It includes an installation of Jupyter Notebook, which presents data science documents that combine live-code with narrative text, equations and visualizations.

Latest version of Python
Various Python packages and libraries are required for web scraping, and must be installed before using this code. 


# Microsoft

This file scrapes financial information from Microsoft Investor Relations (www.microsoft.com/en-us/Investor). Microsoft reports segment revenues by fiscal year quarter. The Jupyter Notebook file extracts quarterly segment revenues and operating expenses for a particular quarter of a fiscal year. The figures are saved to a .csv file, which can be loaded into R.

## Required Packages/Libraries

Requests is a library that will allow us to send HTTP requests to get HTML files. From Requests, the GET method indicates that you’re trying to get or retrieve data from a specified resource. To make a GET request, invoke requests.get()

BeautifulSoup is a Python library for pulling data out of HTML and XML files. This will help us parse the HTML files.

pandas is a Python data analysis library, which will help us assemble the data into a DataFrame to clean and analyze it

NumPy is a Python library used for working with large, multi-dimensional arrays and matrices. It will add support for mathematical functions and tools for working with arrays

The time module in Python has a function sleep() that you can use to suspend execution of the calling thread 

The randint() method returns a pseudo-random integer number 

## Description of code

# Sony

## Required Packages/Libraries

This module provides a portable way of using operating system dependent functionality. 
import os

NumPy is a Python library used for working with large, multi-dimensional arrays and matrices
import numpy as np

wget is a module used to download files
import wget

PDFMiner is a text extraction tool for PDF documents that obtains the exact location of text as well as other layout
information (fonts, etc.), performs automatic layout analysis, and can convert PDF into other formats (HTML/XML)
import pdfminer

## Description of code
