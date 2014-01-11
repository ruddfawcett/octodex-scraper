octodex-scraper
===============

A PHP scraper for http://octodex.github.com. You could use the feedburner RSS and parse that XML, but it doesn't show the author or author avatar, and I wanted to experiment with PHP's DOM.

##Use
The scraper is located at https://octodex-scraper.heroku.com.  You can cURL the page for the [JSON](#json-response), or `file_get_contents` it in PHP, or whatever language you are using.

###Random Octocats
To get a random Octocat, append `?random` to the url: https://octodex-scraper.heroku.com/?random.  The response will be the same as the full Octodex, but it will just be one Octocat (obviously).

##JSON Response
Standard JSON for each Octocat - grabbing a random one, and the whole set.
```json
{
    "name": "original",
    "page": "http://octodex.github.com/original",
    "image": "http://octodex.github.com/images/original.png",
    "author": "http://octodex.github.com/original",
    "number": "1",
    "authorURL": "http://www.idokungfoo.com",
    "authorAvatar": "https://img.skitch.com/20110427-p3wtwcbu957cf9mm93s4sjqqci.png"
}
```

###Keys
- `name` - the name of the octocat
- `page` - the webpage of the octocat
- `image` - the raw image URL of the octocat
- `author` - the creator of the octocat
- `number` - the number of the octocat in the series
- `authorURL` - the URL of the author (GitHub/Website)
- `authorAvatar` - the avatar of the author

##To Do
- Add pagination
- More efficient random octocats

##Use of Octocats
Check out the GitHub Octodex frequently asked questions (http://octodex.github.com/faq), for specific use.  GitHub owns all of the Octocats, this scraper just grabs all of their data.