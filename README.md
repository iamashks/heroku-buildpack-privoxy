# Heroku Privoxy Buildpack

This buildpack installs [Privoxy][1] for your app on Heroku.

> Privoxy is a non-caching web proxy with advanced filtering capabilities for enhancing privacy, modifying web page data and HTTP headers, controlling access, and removing ads and other obnoxious Internet junk. Privoxy has a flexible configuration and can be customized to suit individual needs and tastes. It has application for both stand-alone systems and multi-user networks.

## Setup

With this buildpack installed, Privoxy runs automatically on the port: 8118.

#### Create a new app with this buildpack

Create a new Heroku app with this buildpack (through the [Heroku CLI][2]):

```shell
heroku create --buildpack "https://github.com/iamashks/heroku-buildpack-privoxy.git"
```

#### Or, add this buildpack to an existing app

1] Create a Heroku app as normal with the usual buildpacks.

2] Then, add this buildpack in your app (through the [Heroku CLI][2]):

```shell
$ heroku buildpacks:add https://github.com/iamashks/heroku-buildpack-privoxy.git
```

## Variables

You'll need to provide these as env variables ([check this guide][3]):

* `PRIVOXY_PORT`: The port to be used for the Privoxy server (default: 8118).
* `PRIVOXY_CONF_FILE_URL`: The configuration file for Privoxy (default: supplied).
* `TOR_PROXY_PORT`: The port to be used for the Tor Proxy server (default: 9050).

## Features

* Caches compilation

[1]: https://www.privoxy.org/
[2]: https://devcenter.heroku.com/articles/heroku-cli#getting-started
[3]: https://devcenter.heroku.com/articles/config-vars#using-the-heroku-dashboard
