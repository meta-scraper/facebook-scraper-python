Facebook (Meta) Scraper Python
==============================

Python SDK that allows scraping Facebook (Meta) pages, reviews and more.

`Generate API Token <https://app.outscraper.com/profile>`__

Installation
------------

Python 3+

.. code:: bash

   pip install meta-scraper

`Link to the python package
page <https://pypi.org/project/meta-scraper/>`__

Initialization
--------------

.. code:: python

   from meta_scraper import MetaClient

   client = MetaClient(api_key='API_KEY_FROM_OUTSCRAPER.COM')

Scrape Facebook pages data
--------------------------

.. code:: python

   # Get Facebook pages data
     results = client.get_page_data(['outscraper'])

   ## Scrape Facebook pages reviews

   # Get Facebook pages reviews
     results = client.get_page_reviews(['outscraper'], limit=50)

Facebook pages data demo
------------------------

.. code:: json

   {
     "id": "your-request-id",
     "status": "Success",
     "data": [
       {
         "id": "your-request-id",
         "status": "Success",
         "data": [
           {
             "query": "outscraper",
             "about": "At Outscrpaer, we believe that public data is for everybody, and we apply cutting-edge technologies to prove it.",
             "email": "service@outscraper.com",
             "followers": 45,
             "likes": 43,
             "name": "Outscraper",
             "phone": "+1 281-236-8208",
             "rating": 5,
             "reviews": 6,
             "site": "https://outscraper.com/",
             "types": [
               "App page",
               "Website",
               "Business Service"
             ]
           }
         ]
       }
     ]
   }
