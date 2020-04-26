# Perseus-Minecraft

Perseus-Minecraft is the Minecraft Server setup used on Perseus, an Ubuntu server on our home network.

## Requirements

This setup contains most of the required components to run, but there are a few things you might need to install to run this on a different machine (i.e. not Perseus). Instructions for Debian/Ubuntu are provided, but for all other platforms you can find most of the information you need to get started in [this Minecraft Wiki article](https://minecraft.gamepedia.com/Tutorials/Setting_up_a_server).

The Minecraft Wiki also has a (very, very basic) tutorial on setting up a Minecraft Forge server which can be found [here](https://minecraft.gamepedia.com/Tutorials/Setting_up_a_Minecraft_Forge_server).

### Debian/Ubuntu:

You will need the headless version of OpenJDK 8 to run this server, which can be downloaded and installed via APT using the following command:

```bash
sudo apt-get install openjdk-8-jdk-headless
```

## Usage

Clone the repository, navigate to the project root, and run the [Minecraft Forge](https://www.minecraftforge.net/) JAR file (as root).

If you're running this on a server (i.e. an OS with no GUI, like Perseus's Ubuntu Server OS), remember to use the `nogui` option. Additionally, I would recommend allocating at least 8GB of RAM if available (Perseus allocates 12GB by default).

```bash
sudo java -Xmx12G -Xms12G -jar forge-1.15.2-31.1.0.jar nogui
```

## More Info

### Minecraft Server

The Perseus-Minecraft setup at its core uses the "vanilla" (Mojang developed) Minecraft Server application for *Minecraft: Java Edition*. The JAR file for this application is included in this repository, but it is also [downloadable for free from the official Minecraft site](https://www.minecraft.net/en-us/download/server/).

### Minecraft Mods

This repository includes the necessary files for all the mods and extensions used on the live Perseus server, so you won't need to download them separately, but if you're interested in exactly which mods are used in this setup, you can find a full list in [the MODS file](../blob/master/mods.md).

### Omitted Files

Only a handful of files have been omitted from this repository, and only because they are either specific to the running of the server on a specific machine (i.e. log files), or contain information that should not be published on the internet (i.e. the automatically generated ops.json, usercache.json, usernamecache.json, banned-ips.json, banned-players.json, and whitelist.json files, which all contain information about players, usernames, and user IDs). These files are all kept on the Perseus server itself and can be viewed by users on the Ubuntu OS (**not** by users of the Minecraft Server).

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
