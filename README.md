# alpine-red-discordbot
An Alpine Docker Container with the Red Discord Bot

This Container is based on the latest Alpine Docker-Image and the Red Bot made by Twentysix (https://github.com/Twentysix26/Red-DiscordBot)

## Building

    docker build -t alpine-red-discordbot .
  
## 1st Run

**! BEFORE you start configuring the Bot, make sure you created a Discordaccount for the Bot & invited the account to your server!**

For the first run of the Bot, you need the following Informations:

1. Discordaccount
  * Emailaddress
  * Password
2. Serverroles
  * Name of the Admin-Role
  * Name of the Mod-Role

Run a new Container

    docker run -it -v <your_path>/data:/app/data alpine-red-discordbot

After entering all Informations and installing all cogs, the bot is online and you can check if everything works.
To exit the running Container press CRTL+P and CTRL+Q.

## Run in background

If you want to run your Bot-Container in the Background, you have to stop your "first start"-container, remove them and run a new one:

    docker run -d --name <your_container_name> -v <your_path>/data:/app/data alpine-red-discordbot

It should load the config from *<your_path>/data*  

## How to use the Bot

See the Wiki https://github.com/Twentysix26/Red-DiscordBot/wiki
