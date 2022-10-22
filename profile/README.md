# mana9er: a daemon framework for Minecraft
mana9er is a daemon framework for Minecraft. It monitors a Minecraft server and provides API to interact with the server. The framework itself provides only API, so you need to use mana9er plugins to get additional features, like backup and restoration system, tps monitor, and chat forwarding.

mana9er acts entirely as an external daemon, that is, it interacts with the Minecraft server via standard I/O, just like an operator sitting in front of the console and typing commands reacting to the server output. As a result, it doesn't affect the game data at all, and you can add or remove it at any time without worrying about compatibility issues.

## API

For developer's guide, see [how-it-works](https://github.com/mana9er/.github/blob/master/docs/en/how-it-works.md) and [api](https://github.com/mana9er/.github/blob/master/docs/en/api.md).

## Deploy

For deployment guide, see [deployment](https://github.com/mana9er/.github/blob/master/docs/en/deploy-mc.md).

## Plugin Examples

+ [mcBasicLib](https://github.com/mana9er/mc-mcBasicLib): Prerequisite of some plugins. It provides signals and methods about Minecraft game logic.
+ [scoreboardHelper](https://github.com/mana9er/mc-scoreboardHelper): Switching in-game sidebar scoreboard.
+ [multiChat](https://github.com/mana9er/mc-multiChat): Chat forwarding.
+ [saveload2](https://github.com/mana9er/mc-saveload2): Backup, auto backup and restoration.
+ [aliyun-saveload](https://github.com/mana9er/mc-aliyun-saveload): Backup, auto backup and restoration with cloud object storage of Aliyun.
+ [easyMark](https://github.com/mana9er/mc-easyMark): In-game memo.
+ [easyCalc](https://github.com/mana9er/mc-easyCalc): In-game calculator.
+ [cmdRepost](https://github.com/mana9er/mc-cmdRepost): Provide some in-game commands.

## Demo Screenshots

Initializing several plugins during startup:

![](https://github.com/mana9er/.github/blob/master/docs/img/startup.png?raw=true)

Help message of the plugin saveload2:

![](https://github.com/mana9er/.github/blob/master/docs/img/sl_help.png?raw=true)

Listing backups:

![](https://github.com/mana9er/.github/blob/master/docs/img/sl_list.png?raw=true)
