## Overview

To use ***mana9er*** to manage your Minecraft server and experience various plugins:

1. Download your Minecraft server and remember the path. Generally any version after 1.13 is OK.
2. Clone the mana9er-core from [github](https://github.com/mana9er/mana9er-core).
3. Modify the configuration file `config.json` (which will be further discussed in the next section)
4. Select your plugins and install them by placing plugin folders under mana9er-core folder. Your mana9er-core folder should look like:
```
.
├── README.md
├── config.json
├── core.py
├── log.py
├── utils.py
├── requirements.txt
├── easyMark
│   ├── __init__.py
│   └── ...
├── cmdRepost
│   ├── __init__.py
│   └── ...
├── saveload
│   ├── __init__.py
│   └── ...
└── main.py
```

Don't forget to install required packages for mana9er-core and all your plugins. Then, just run `python3 main.py` to start your server under mana9er framework. After it starts running, you are able to interact through console, typing commands or receiving outputs.

## Config

A sample config file would be like:

```json
{
    "default_entrance":{
        "wd": "/path/to/your/minecraft-server/",
        "exec": "java -Xms512m -Xmx2048m -jar forge-1.15.1-30.0.18.jar nogui"
    },
    "plugins": ["mcBasicLib", "easyMark", "saveload"],
    "log_level": 2,
    "prefix": "#"
}

```

`wd` indicates the working directory of mana9er, which should be the directory of your Minecraft server. `exec` will be directly executed to start Minecraft server in a subprocess and you can appoint some arguments for your server, such as memory limits.

In `plugins`, you should include all plugins you wish to enable and make sure the corresponding folders exist. The plugins will be loaded following the order of this list, so if plugin B depends on plugin A, make sure you write plugin A first.

`log_level` controls the output level of the logger. 0, 1, 2, 3 stands for DEBUG, INFO, WARNING and ERROR, respectively. Only logs with level higher or equal to `log_level` will be printed. If you want a clear console, level 3 is recommended.

`prefix` controls the prefix of built-in commands. For example, if `prefix` is set to "#", then when you type "#start", "#stop", "#restart" or "#quit", they will be interpreted as built-in commands of mana9er core (*start*, *stop*, *restart* the server, or *quit* mana9er immediately). If your command doesn't start with `prefix`, it will be considered as other command (e.g. a command defined by a plugin) and be processed differently.
