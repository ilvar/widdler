widdler
=======

widdler is a single binary that serves up
[TiddlyWiki](https://tiddlywiki.com)s.

It can be used to server existing wikis, or to create new ones.

# Features

- TiddlyWikis are served over WebDav so you can save directly from the browser.
- Automatically create new wiki files by browsing to a non-existent html file.
- Built in .htpasswd management (Adding users).
- Password protection via HTTP Basic Authentication.
- Multiple users (adding another user to the .htaccess file creates a new user
  namespace).
- Optional TLS support.

# Installation

```
go get -u suah.dev/widdler
```

# Running

```
mkdir wiki
cd wiki
# Generate a .htpasswd file:
widdler -gen
Username: qbit
Passwd: ******
./widdler
```

Now open your browser to [http://localhost:8080](http://localhost:8080).

# Creating a new TiddlyWiki

Simply browse to the file name you wish to create. widdler will automatically
create the wiki file based off the current `empty.html` TiddlyWiki version.

# Saving changes

Simply hit the save button!

