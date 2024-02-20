# Nvidia Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Nvidia Scraper](https://oxylabs.io/products/scraper-api/ecommerce/nvidia?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Nvidia website effortlessly. This brief guide showcases how Nvidia Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Nvidia results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Nvidia page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.nvidia.com/en-us/geforce/graphics-cards/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/nvidia-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n<!DOCTYPE HTML>\n<html class=\"html-page no-js\" xmlns=\"http://www.w3.org/1999/xhtml\" lang=\"en-us\" xml ... </html>",
      "created_at": "2024-02-20 12:35:54",
      "updated_at": "2024-02-20 12:35:55",
      "page": 1,
      "url": "https://www.nvidia.com/en-us/geforce/graphics-cards/",
      "job_id": "7165685496922775553",
      "status_code": 200
    }
  ]
}
```
Use our Nvidia Scraper to seamlessly harvest publicly available data from all Nvidia platforms. Gather essential details like product specifications, release dates, or software updates to keep abreast of industry developments and gain an edge over your rivals. If you encounter any issues, feel free to reach out to our customer service team through live chat or drop us an email at support@oxylabs.io.