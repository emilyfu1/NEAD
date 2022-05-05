This file provides the documentation for my web scraping project as a student employee with Statistics Canada. These web scraping scripts aim to retrieve financial reports and price information from various online sources. 


# Configuration/Installation

Anaconda is a distribution of the Python and R programming languages for scientific computing (data science, machine learning applications, large-scale data processing, predictive analytics, etc.), that aims to simplify package management and deployment. It includes an installation of Jupyter Notebook, which presents data science documents that combine live-code with narrative text, equations and visualizations. 

The web scraping code is written in Python. The latest version of Python should be installed. Various Python packages and libraries are required for web scraping, as detailed in each file, and must be installed before running the code. A list of approved packages is stored in Artifactory. New packages can be requested through Jira.

# files included

## microsoft.ipynb
File for scraping Microsoft financial data.

## sony.ipynb
File for downloading Sony financial statements.

## canadacannabisdispensary.ipynb
File for recording price information from Canada Cannabis Dispensary.

## cheebas.ipynb
File for recording price information from Cheebas.

## rosebudremedy.ipynb
File for recording price information from Rosebud Remedy.

## speedgreens.ipynb
File for recording price information from Speedgreens.

# Use

Web scraping involves parsing the HTML of a webpage to automate the retrieval and structuring of data from online sources instead of manually entering and manipulating data. 

Beautiful Soup is an important library in web scraping applications. 
The documentation for the Beautiful Soup library can be found here: https://beautiful-soup-4.readthedocs.io/en/latest/

## Microsoft

This file scrapes financial information from Microsoft Investor Relations (www.microsoft.com/en-us/Investor). Microsoft reports segment revenues by fiscal year quarter. The Jupyter Notebook file extracts quarterly segment revenues and operating expenses for a particular quarter of a fiscal year. The figures are saved to a .csv file, which can be loaded into R or used for other data analysis purposes.

The code searches for an existing CSV file with previous data, and creates one if no file exists. It uses dataframes and the BeautifulSoup library to create a panel dataset of financial 

### Operating Instructions

To open the file, navigate to the directory in Jupyter Notebook and click on the filename. A single block of code can be run by selecting the block and clicking "Run" at the top of the Jupyter Notebook interface. This will only run the selected block. Separate blocks correspond to separate actions the code can undertake.

## Sony

This file downloads PDF files from Sony Investor Relations (https://www.sony.com/en/SonyInfo/IR/library/presen/er/archive.html) into a specified directory. Sony does not provide the required financial information in HTML format, but downloading the PDF files through the code instead of manually downloading should be a time-saving process. The code also converts the downloaded files to HTML, but these conversions are difficult to scrape using BeautifulSoup due to the formatting of PDFs and the lack of distinction between relevant and irrelevant tables. Nevertheless, they may provide useful information in the future

### Operating Instructions

To open the file, navigate to the directory in Jupyter Notebook and click on the filename. A single block of code can be run by selecting the block and clicking "Run" at the top of the Jupyter Notebook interface. This will only run the selected block. Separate blocks correspond to separate actions the code can undertake.

Using this code, you can download and convert a range of PDF files by running the first and second code blocks, or download and convert a single file with the first and third code blocks.

## Illegal cannabis websites

This file scrapes price data from various illegal cannabis delivery websites. The Jupyter Notebook file extracts prices for relevant products. The figures are saved to a .csv file, which can be loaded into R or used for other data analysis purposes.

Canada Cannabis Dispensary, Speedgreens, and Cheebas are illegal cannabis delivery websites. Rosebud Remedy is a company that produces edibles and various cannabis products. Prices for these goods are listed on the Canada Cannabis Dispensary website. The corresponding files can be used to gather information on the prices of select cannabis goods over time

### Operating Instructions

To open the file, navigate to the directory in Jupyter Notebook and click on the filename. A single block of code can be run by selecting the block and clicking "Run" at the top of the Jupyter Notebook interface. This will only run the selected block. Separate blocks correspond to separate actions the code can undertake.

The code searches for an existing CSV file with previous data, and creates one if no file exists. It uses dataframes and the BeautifulSoup library to create a panel dataset of relevant products. Using this code, prices as currently displayed on the relevant webpage will be appended to existing data.

## Maintaining and updating code

Web scraping scripts are written with the HTML of a specific webpage in mind. If the appearance or design of a webpage changes, the code may no longer work to retrieve the necessary information. Before updating or rewriting any code, the HTML of a website should be inspected to determine how and where the data is stored. This may require basic familiarity with HTML and CSS.

URLs determine the web location(s) of the information you are trying to obtain, and may also change. In particular, illegal cannabis delivery websites tend to reappear after being taken down, but under a new domain. The Canada Cannabis Dispensary website was taken down during March and April 2022 and was not accessible at the time. If a new website returns under a different URL, the URL should be updated in the code. 

A further step in the implementation of this process may involve further automation; instead of running the script for each source when necessary, it may be possible to arrange for the code to run automatically at set intervals (e.g. monthly)
