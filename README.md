# Bootstrap CDN

[![Join the chat at https://gitter.im/MaxCDN/bootstrap-cdn](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/MaxCDN/bootstrap-cdn)
[![Build Status](https://travis-ci.org/MaxCDN/bootstrap-cdn.svg?branch=master)](https://travis-ci.org/MaxCDN/bootstrap-cdn)
[![dependencies Status](https://david-dm.org/MaxCDN/bootstrap-cdn/status.svg)](https://david-dm.org/MaxCDN/bootstrap-cdn)
[![devDependencies Status](https://david-dm.org/MaxCDN/bootstrap-cdn/dev-status.svg)](https://david-dm.org/MaxCDN/bootstrap-cdn?type=dev)


## Deploy your own copy on Heroku

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)


## Requirements

1. [Node.js](https://nodejs.org/)

## Running

Use `node make <task>`.

### Development

```sh
npm install

node make test run
```


### Demonized

```shell
##
# for the following make tasks, you can also run:
#
# npm run <task name>
##

# start server
node make start

# stop server
node make stop

# restart server
node make restart

# server status
node make status

# view logs
node ./node_modules/.bin/forever logs app.js
```

## Configuration

### `config/_config.yml`

Key Overview:

1. `port`: Integer value of the Node application port.
2. `theme`: Integer value of the array index from the `bootswatch` section below.
3. `authors`: Array of author Strings
4. `description`: String containing the meta description of the site.
5. `favicon`: Hash containing the favicon path.
6. `google_analytics`: Hash containing GA `account_id` and `domain_name`.
7. `stylesheets`: Array containing stylesheet files to be loaded at the top of the site.
8. `javascripts`: Array containing JavaScript files to be loaded either `before` (at the top) or `after` (at the bottom) of the site.
9. `bootswatch`: Hash containing current Bootswatch meta data and themes.
10. `bootlint`: Array of hashes containing Bootlint meta data and pathing.
11. `bootstrap`: Array of hashes containing Bootstrap meta data and pathing.

### `config/_tweets.yml`

To add new tweets to the "Mad Love" section, follow these steps:

1. Copy the full `<blockquote>` HTML from the "Embed Tweet" source obtained via Twitter.
2. Replace all double quotes (`"`) with single quotes (`'`).
3. Wrap entire HTML block in double quotes (`"`).
4. Add to `_tweets.yml`, preceeded with a dash (`-`), which signifies an array item in YAML.

### `config/_oauth.yml`

This is reserved for MaxCDN and NetDNA installation only at this time.
Contact [@jdorfman](https://github.com/jdorfman) for more information.
