# Flickr_Scraper
Flickr Image Scraper: Look inside the 'if __name__ == '__main__':' and the 'run' function to see examples and notes on how to run.

modules required:
```python
import time, requests, re, os
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from bs4 import BeautifulSoup
```

Can scrape images given links to a [photostream](https://www.flickr.com/photos/141159174@N07/) or an [album.](https://www.flickr.com/photos/parismadrid/albums/72157652417586970)

Can also be given as keyword (such as ['dog'](https://www.flickr.com/search/?text=dog)).

Note: Searching with a keyword involves (automated) scrolling and loading a lot of images, so I recommend photostreams and albums if possible. I wonder if this is Flickr's way of preventing anyone from easily stealing their millions of dog images.


#### Flickr_Fast 
Pro: 
- Fast.
- Can decide what size you want. Default is 'large' (tag 'b') and this worked great for me as most images have this size available and it is a quality good enough for me. 
- Keyboard interrupt supported 

Con: 
- Will give an unavailable image if specified size does not exist (search will continue with next image)



#### Flickr_Slow
Pro: 
- Guaranteed to get you the largest possible size (the robust, quality alternative if you have fast internet and want every picture at the biggest size)

Con: 
- Slow for two reasons: download will take longer and the implementation to get these images involved jumping through more hoops


#### Comparison to manual downloads without this program
- Albums: Program downloads albums for users faster than Flickr does
- Keyword and photostream mass downloads: Feature not available in Flickr 


