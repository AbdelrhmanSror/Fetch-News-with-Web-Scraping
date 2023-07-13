# Fetch-News-with-Web-Scraping Readme

This Jupyter Notebook provides a script for web scraping news articles from a website and storing them in a Pandas DataFrame. It uses the BeautifulSoup library for web scraping and the requests library for downloading web pages.

## Installation

Before running the notebook, you need to install the required dependencies. You can do this by executing the following commands in a code cell:

```python
!pip install html5lib
!pip install bs4
```

## Usage

1. Import the necessary libraries by executing the code cell:

```python
from bs4 import BeautifulSoup
import requests
import pandas as pd
```

2. Set up the configuration by defining the types of news and the base URL in the code cell:

```python
types = {
    "politics": "سياسة",
    "ebusiness": "اقتصاد",
    "culture": "ثقافة",
    "sport": "رياضة",
    "arts": "فن",
    "tech": "تكنولوجيا",
    "turath": "تراث",
    "midan": "ميدان"
}

base_url = "https://1-a1072.azureedge.net"
```

3. Download the HTML of the news pages by executing the code cell:

```python
for key in types:
    downlaod_html_news(key)
```

4. Extract the news articles for each type and append them to a Pandas DataFrame by executing the code cell:

```python
def extract_news_with_type_and_append_to_dataframe(_type):
    # ...
    return data

data = pd.DataFrame(columns=["Type", "Header", "Body", "Date", "URL"])

for key in types:
    news_data = extract_news_with_type_and_append_to_dataframe(key)
    data = pd.concat([data, news_data], ignore_index=True)
```

5. View the extracted news articles by executing the code cell:

```python
data
```
