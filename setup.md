# Setting Up Jetski

## Adding the Bot

Rowfox is a private bot, if the bot has been added to your server, then read on below.

## How to Set Up

Once Rowfox has been added to your server, go to [https://rowfox.recothefolf.tech/](https://rowfox.recothefolf.tech/) to edit your server's configuration. Use the sidebar to read about each plugin, then use the example below along with the information in the sidebar to set up your own customized Rowfox configuration.

Below is a blank configuration example with web, utilities, admin, infractions, modlog, spam, and censor set up. While you can simply copy-paste this to your own server's configuration and fill in the blanks to have a perfectly usable Rowfox, it's highly encouraged that you read through the full documentation to understand each component and customize Rowfox to your server's needs.

```text
web:
  000000000000000000: admin #Username
  000000000000000000: editor #Username
  000000000000000000: viewer #Username

commands:
  prefix: '!'
  overrides: []

levels:
  000000000000000000: 000 # Role

nickname: Rowfox

plugins:

  utilities: {}

  admin: {}

  infractions:
    mute_role: 000000000000000000

  modlog:
    channels:
      00000000000000000000000:
        exclude: []
        include: []
    ignored_users: []

  spam:
    levels:
      0:
        punishment: TEMPMUTE
        punishment_duration: 120
        max_messages:
          count: 10
          interval: 7
        max_mentions:
          count: 8
          interval: 30
        max_links:
          count: 10
          interval: 60
        max_emojis:
          count: 100
          interval: 120
        max_newlines:
          count: 60
          interval: 120
        max_duplicates:
          count: 5
          interval: 30

  censor:
    levels:
      0:
        filter_invites: true
        invites_whitelist: ['discord-testers', 'discord-feedback']
        blocked_words: ['word1', 'word2', 'word3']
```

