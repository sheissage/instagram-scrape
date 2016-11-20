<img src="http://i.imgur.com/iH2jdhV.png" align="right" />

Instagram Scraper
=================
Instagram-Scraper is a command-line application written in Python that scrapes and downloads an instagram user's photos and videos. Use responsibly.

Install
-------
To install the project dependencies:
```bash
$ python setup.py install
```

If you don't want to install it globally, you can use virtualenv:
```bash
$ virtualenv venv
$ source venv/bin/activate
$ python setup.py install
```

Usage
-----
To scrape a public user's media:
```bash
$ instagram-scraper <username>             
```

To specify multiple users, pass a delimited list of users:
```bash
$ instagram-scraper username1,username2,username3           
```

You can also supply a file containing a list of usernames:
```bash
$ instagram-scraper -f ig_users.txt           
```
```
# ig_users.txt

username1
username2
username3
# and so on...
```
The usernames may be separated by newlines, commas, semicolons, or whitespace.

To specify the download destination:
```bash
$ instagram-scraper <username> -d /path/to/destination
```
By default, media will be download to *`<current working directory>/<username>`*

To scrape a private user's media when you are an approved follower:
```bash
$ instagram-scraper <username> -u <your username> -p <your password>
```


Develop
-------

Clone the repo and create a virtualenv 
```bash
$ virtualenv venv
$ source venv/bin/activate
$ python setup.py develop
```

Running Tests
-------------

```bash
$ python setup.py test

# or just 

$ nosetests
```

Contributing
------------

1. Check the open issues or open a new issue to start a discussion around
   your feature idea or the bug you found
2. Send a pull request

License
-------
This is free and unencumbered software released into the public domain for education or testing purposes.
