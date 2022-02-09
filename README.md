# Assignment2-Django
## Installation

First, set up your project with django by creating app and templates.

If you have pip on your system, you can simply install **selenium**, **BeautidulSoup 4**.

To get the data from https://etherscan.io/accounts, we need to register and create new API Key to fully access to API.

Charts are created by Chart.js library.

We also need to use webdriver package to page 100 accounts visible and scrape them.

## Usage
* Import those libraries
* Open a new Firefox browser
* Load the page at the given URL
### Example 1
```
url = 'https://etherscan.io/accounts'
driver = webdriver.Firefox()
driver.get(url)
```
* Parse the web page using BeautifulSoup as soup
* Toke the news articles using find_all() method
* Print them out taking only text that is inside tags
### Example 2
BeautifulSoup is used to scrape lines that placed in 'a' tag.
```
page = driver.page_source

soup = BeautifulSoup(page, 'html.parser')

attrs = soup.find_all('a')
```

### Example 3
All the addresses and balances a stored in sqlite3 that is integrated with Django project. You can also manage the data and add new data by accessing the admin page.
