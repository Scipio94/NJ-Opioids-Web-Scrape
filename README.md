# NJ Opioids Web Scrape
Retrieving suspected drug deaths data for January 1, 2024 through June 30, 2024 using the scrapy python package!

## To complete a Web Scrape Follow the steps below:

### 1. Import packages
- from scrapy import Selector
- import requests as r

### 2. Instantiate relevant objects for scrapy
- url = 'https://...'
- html = r.get(url).content
  - The ***content*** attribute retrieves the raw binary content of the response body
  - retrieve html via GET request
  - If a 403 code is returned on the initial GET request create a User-Agent
      - A User-Agent includes information about the browser, operating system, and device being used
  - sel = Selector(text = html)
    - Instansiating the selector object to navigate html via xpath or css notation.

### 3. Navigate Web Page
- sel.xapth('/html....')
