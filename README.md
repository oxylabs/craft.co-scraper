# Craft.co Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Craft.co Scraper](https://oxylabs.io/products/scraper-api/web/craftco?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Craft.co website effortlessly. This brief guide explains how an Craft.co Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Craft.co results by providing your own URLs to our service. We can return the HTML for any Craft.co page you like.

#### Python code example

The example below illustrates how you can get HTML of Craft.co page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://enterprise.craft.co/craft-api'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/craft.co-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><!-- Last Published: Tue Oct 24 2023 19:49:44 GMT+0000 (Coordinated Universal Time) - ... </html>",
      "created_at": "2023-12-18 11:08:18",
      "updated_at": "2023-12-18 11:08:19",
      "page": 1,
      "url": "https://enterprise.craft.co/craft-api",
      "job_id": "7142470627675373569",
      "status_code": 200
    }
  ]
}
```
With our Craft.co Scraper, you can seamlessly gather pertinent company data from all Craft.co web pages. Acquire the necessary business insights, such as key financials, team size, or headquarters location, to evaluate the market and outpace your business competitors. For any queries, please reach out to our support team via live chat or email us at hello@oxylabs.io.