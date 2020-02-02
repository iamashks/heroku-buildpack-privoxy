# Heroku Privoxy Buildpack

This buildpack installs [Privoxy](https://www.privoxy.org/) within a dyno, with the default Privoxy config.

> Privoxy is a non-caching web proxy with advanced filtering capabilities for enhancing privacy, modifying web page data and HTTP headers, controlling access, and removing ads and other obnoxious Internet junk. Privoxy has a flexible configuration and can be customized to suit individual needs and tastes. It has application for both stand-alone systems and multi-user networks.

The server will be running on 8118.

## Configuration

Currently will need to provide your own config file if you want anything other than the defaults in `extra/config`

## Use

Create a Heroku app with this buildpack
```shell
heroku create --buildpack "https://github.com/iamashks/heroku-buildpack-privoxy.git"
```
Set the buildpack for an existing Heroku app

```shell
heroku buildpacks:set https://github.com/iamashks/heroku-buildpack-privoxy.git
```
