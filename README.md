heroku-buildpack-exiftool
=========================

A Heroku buildpack that installs the Phil Harvey's [ExifTool](http://www.sno.phy.queensu.ca/~phil/exiftool/).

## How it works

ExifTool installation ends in `/app/vendor/exiftool` directory.

Usage
-----

## Configure from CLI

```bash
heroku buildpacks:add https://github.com/velizarn/heroku-buildpack-exiftool
```

## Configure from app manifest

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

## Example usage

```
-----> exiftool app detected
       Custom Exiftool URL is not set, start downloading from default location
-----> Installing exiftool 11.32
       Fetching   https://www.sno.phy.queensu.ca/~phil/exiftool/Image-ExifTool-11.32.tar.gz
       Installed: exiftool
-----> Discovering process types
```

### Add custom download location

If you prefer to deploy your own archve you can set a config var to download Exiftool from a custom location, e.g.

```bash
heroku config:set EXIFTOOL_URL_CUSTOM=https://123456.mycdn.org/downl/Image-ExifTool-11.36.tar.gz
```
```
-----> exiftool app detected
      Start downloading Exiftool from https://123456.mycdn.org/downl/Image-ExifTool-11.36.tar.gz
-----> Installing exiftool 11.36
      Fetching   https://123456.mycdn.org/downl/Image-ExifTool-11.36.tar.gz
      Installed: exiftool
-----> Discovering process types
```

## Resources

- [ExifTool by Phil Harvey](https://www.sno.phy.queensu.ca/~phil/exiftool/)
- [ExifTool Revision History](http://owl.phy.queensu.ca/~phil/exiftool/rss.xml)

## License

MIT
