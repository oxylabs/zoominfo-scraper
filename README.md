# Zoominfo Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Zoominfo Scraper](https://oxylabs.io/products/scraper-api/web/zoominfo?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Zoominfo website effortlessly. This brief guide explains how an Zoominfo Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Zoominfo results by providing your own URLs to our service. We can return the HTML for any Zoominfo page you like.

#### Python code example

The example below illustrates how you can get HTML of Zoominfo page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.zoominfo.com/pricing'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/zoominfo-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" /><meta name=\"viewport\" content=\"width=de ... </html>",
      "created_at": "2023-12-18 10:43:31",
      "updated_at": "2023-12-18 10:43:33",
      "page": 1,
      "url": "https://www.zoominfo.com/pricing",
      "job_id": "7142464392305604609",
      "status_code": 200
    }
  ]
}
```
With our Zoominfo Scraper, you can deftly compile accessible data from any Zoominfo web page. Harvest vital business information, including company revenue, industry type, or executive contact details, to enhance your B2B relations and ace your game in the market. If you require any assistance, our support team is ready to help through our live chat or you can reach out to us via email at hello@oxylabs.io.