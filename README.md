## Flickr_Scraper
Flickr Image Scraper

#Flickr_Fast 
will get the image of the size you want. Default is large (tag 'b') and this worked great for me as most images have this size available. 
Pro: Fast, can decide what size you want 
Con: Doesn't automatically fetch the biggest image, will give an unavailable image if specified size does not exist (but code won't break)

#Flickr_Slow
Pro: will get you the largest possible size
Con: slow for two reasons- download will take longer and the implementation to get these images involved jumping through more hoops

Look inside the 'if __name__ == '__main__':' of the two files and look at the 'run' function to see example and notes.
