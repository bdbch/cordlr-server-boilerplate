# Cordlr Server Boilerplate

This is a server boilerplate for the Discord bot framework [**Cordlr**](https://github.com/Devcord/cordlr-cli).

You can use this boilerplate to setup a server without setting up the configuration by your own. Just follow the instructions and watch your bot breathe!

## Setup

Clone this repository or download the zip file to your computer and put it into a specific folder, for example `~/discord-server`. Change into the new server and run `npm install` *(Make sure to use Node.js 6+)* to install the cordlr packages. After NPM installed the packages you are ready to configure your bot.

1) Do `npm install` in terminal
2) Configure your `cordlr.json` file (Read **Configuration** below)
4) Do `npm start` in terminal
3) Add bot to your Discord server ([Discord Docs](https://discordapp.com/developers/docs/topics/oauth2#adding-bots-to-guilds))
    * Go to [Discord API](https://discordapp.com/developers/applications/me) and open what you just created in **Configuration**
    * Get your **Client ID**
    * https://discordapp.com/api/oauth2/authorize?client_id=**`<Your Client ID>`**&scope=bot&permissions=0

## Configuration

Open the **cordlr.example.json** and add your bot token so your bot can actually login. You can retrieve your bots token from the [Discord API](https://discordapp.com/developers/applications/me). Save the file as **cordlr.json**

* **token**: Your bot token. Is used to authenticate the bot
* **prefix**: The bot prefix which will trigger your bot. `!` by default
* **plugins**: Array containing all loaded plugins with the *cordlr-* prefix. Make sure to install the packages before adding them here
* **plugin specific configuration**: every plugin can load values from here. Read your installed plugins documentation for configuration values

**IMPORTANT NOTE**: Make sure to not push your private bot token to Github or any other public site.

## Installed Plugins

By default the following plugins are installed:

* **cordlr-help2**: Lists all commands & plugins with usage info and descriptions using **!help** or **!plugins**
* **cordlr-ddg**: DuckDuckGo package allows searching for topics and use of DDG !bangs via **!ddg <search>**
* **cordlr-giphy**: Retrieves a random giphy via **!giphy** or **!giphy <tag>**
* **cordlr-roles**: Allows users to manually join certain, whitelisted roles via **!addrole <role>**, **!removerole <role>** and **!roles**
* **cordlr-kontrolla**: Administrator tool to control the bot (change avatar, game and username)

## Contribute

Hop over to [Cordlr CLI](https://github.com/Devcord/cordlr-cli) to help us!
