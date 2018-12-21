# Scrape the web because you're bad at documentation :)

Since 2010, [Babycastles](http://babycastles.com) has been throwing great events and doing a bad job documenting them. It's hard to describe what we do without photos and videos so I'm documenting the tools and process I use to scrape social media sites for photos of our events. 

I'm writing these using a Mac, if it's different for a PC/Linux - sorry. Hope this helps other people too.

## Downloading from Instagram
This will save the videos & photos and save the filename with the date it was posted to instagram & the username who posted it. the files look like this "2012-10-10_02-09-30_UTC_babycastles.jpg"

1. Uning Terminal, install [pip](https://pip.pypa.io/en/stable/installing/), if its not on your machine
2. Install [Instaloader](https://instaloader.github.io/) using pip `pip install instaloader`
3. Download all Babycastles posts tagged (both with and '@' and a '#') & posted to our account using this command:
`instaloader --login=babycastles babycastles '#babycastles' --filename-pattern={date_utc}_UTC_{profile} --tagged --comments`
4. Download all posts with the hashtag #babycastles using:
`instaloader --login=babycastles "#babycastles" --filename-pattern={date_utc}_UTC_{profile}`
5. And anything posted to our location_id (271251592)
*this doesn’t seem to work yet but it was [just released](https://github.com/instaloader/instaloader/pull/212) 5 hours before I tried it so maybe it still has some bugs to work out. i'm on 4.1.1, try `pip install --upgrade instaloader later`*
`instaloader --login=babycastles "%271251592" --filename-pattern={date_utc}_UTC_{profile}`
6. After you download everything once, you can just append `--fast-update` and it will only download the latest posts since the last time you ran the query

## Downloading from YouTube
1. Install [youtube-dl](https://rg3.github.io/youtube-dl/) `sudo pip install --upgrade youtube_dl`
