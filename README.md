# WP CLI Sync

A WP-CLI command for syncing a live site to a development environment

![WP-CLI Screenshot](https://i.imgur.com/ugUhcuQ.gif)

## Requirements

* A [bedrock](https://github.com/roots/bedrock) based WordPress project
* [WP-CLI](https://github.com/wp-cli/wp-cli)
* [rsync](https://rsync.samba.org)

## Installation

1. Require the plugin by running:

```sh
composer require jonbp/wp-cli-sync
```

2. Add the following to your `.env` file (don't forget `.env.example` for reference 😉):

```sh
# WP-CLI Sync Settings [wp sync]
LIVE_SSH_HOSTNAME=""
LIVE_SSH_USERNAME=""
REMOTE_PROJECT_LOCATION="~/gitrepo"

# Plugins should be formatted in a comma seperated format
# For example: "plugin1,plugin2,plugin3"

# Plugins activated on sync
DEV_ACTIVATED_PLUGINS=""

# Plugins deactivated on sync
DEV_DEACTIVATED_PLUGINS=""

# Dirs to exclude from sync
# Multiple dirs can be provided by separating with a comma
# Use dir names or paths relative to uploads dir
DEV_SYNC_DIR_EXCLUDES=""

# DB Queries to run after sync
DEV_POST_SYNC_QUERIES=""

```

3. Run `wp sync` from the project root.
