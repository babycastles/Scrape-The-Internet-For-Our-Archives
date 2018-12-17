# Scrape the web because we're bad at documentation :)
Since 2010, Babycastles has been great at hosting events and bad at documenting them. When we describe what we do, it's hard to do that without pictures and videos! 

I'm documenting the tools and process I use to scrape social media sites to help capture the photos & videos people have taken and shared at our space. I'm writing these using a Mac, if it's different for a PC/Linux - sorry.

## Download from Instagram
1. Install [pip](https://pip.pypa.io/en/stable/installing/), if its not on your machine
2. Install [Instaloader](https://instaloader.github.io/) using pip
3. Download all posts tagged & posted to an account using this:
`instaloader --login=babycastles babycastles --filename-pattern={date_utc}_UTC_{profile} --tagged --comments`
