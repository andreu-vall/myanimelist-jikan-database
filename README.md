# MyAnimeList Jikan Database

Scraping of the MyAnimeList Jikan REST API's internal database (Anime, Manga, Characters and People)

The scraping is really simple and doesn't require anything but Python and an Internet connection. It's done in the scraping.ipynb file.

The Jikan API allows 60 requests / minute, so the scraping is done at 1 call per 1.2 seconds (slightly less crashes).
Every call to the API returns 25 entries, so the time to scrape each Dataset is simply number_entries * 1.2 / 25 seconds, which means:

- 24 640 Animes takes 20 min
- 146 049 Characters takes 2 hours
- 66 371 Mangas takes 55 min
- 16 943 People takes 14 min

The scraped Data has been recenlty uploaded on [kaggle](https://www.kaggle.com/datasets/andreuvallhernndez/myanimelist-jikan) (scaped on 17 July 2022), feel free to use it.
