# Scrape the web because we're bad at documentation :)
Since 2010, Babycastles has been great at hosting events and bad at documenting them. When we describe what we do, it's hard to do that without pictures and videos! 

I'm documenting the tools and process I use to scrape social media sites to help capture the photos & videos people have taken and shared at our space. I'm writing these using a Mac, if it's different for a PC/Linux - sorry.

## Download from Instagram
This will save the videos & photos and save the filename with the date it was posted to instagram & the username who posted it.

1. Install [pip](https://pip.pypa.io/en/stable/installing/), if its not on your machine
2. Install [Instaloader](https://instaloader.github.io/) using pip
3. Download all Babycastles posts tagged (both with and '@' and a '#') & posted to our account using this command:
`instaloader --login=babycastles babycastles '#babycastles' --filename-pattern={date_utc}_UTC_{profile} --tagged --comments`
4. Download all posts with the hashtag #babycastles using:
`instaloader --login=babycastles "#babycastles" --filename-pattern={date_utc}_UTC_{profile}`
5. And anything posted to our location_id (271251592)
*this doesn’t seem to work yet but it was [just released](https://github.com/instaloader/instaloader/pull/212) 5 hours before I tried it so maybe it still has some bugs to work out*
`instaloader --login=babycastles "%271251592" --filename-pattern={date_utc}_UTC_{profile}`
