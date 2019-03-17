heroku-buildpack-exiftool
=========================

A Heroku buildpack that installs the latest production version of Phil Harvey's [ExifTool](http://www.sno.phy.queensu.ca/~phil/exiftool/).

Usage
-----

Add this Git repo to buildpacks list in your app.json file, e.g.:
```
"buildpacks": [
  {
    "url": "heroku/nodejs"
  },
  {
    "url": "https://github.com/velizarn/heroku-buildpack-exiftool.git"
  }
]
```
