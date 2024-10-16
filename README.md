# Zerops x Quake 3

Do you ever feel a wave of nostalgia, yearning to play classic first-person shooters like **Quake 3: Arena**, but dread the thought of spending hours configuring a server? We've got the perfect solution for you! Here's a quick and easy way to start your own Quake 3: Arena server and dive into nostalgic gameplay with your friends in no time.


![quake](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/svg/cover-quake.svg)


## Using LinuxGSM

We'll be using [LinuxGSM](https://linuxgsm.com/) to deploy this game server. LinuxGSM (Linux Game Server Managers) is a command-line tool for deploying and managing dedicated game servers on Linux.

For more advanced configuration options, you can refer to the [official LinuxGSM Quake 3: Arena server documentation](https://linuxgsm.com/servers/q3server/).

<br/>

## Deploy on Zerops

To deploy your Quake 3: Arena server on Zerops, follow these steps:

1. Set up your Zerops account and project (if you haven't already).
2. Create a new service for your (e.g. ```quake3-server```)
3. To ensure your server functions correctly, you need to enable IPv4 connectivity. Follow these extra steps in the Zerops GUI:

- Projects > `quake3-server`
    - IP Addresses & Public Routing Overview > (Activate) Unique IPv4 address
    - Services > `q3server` > Public access & internal ports > Public Access through IP Addresses > Setup up the first
      access through IPv4

You can change server some of the server configuration parameters by changing following environment variables in `zerops-import.yml` or `zerops.yml`.

| key           | type          | default                                   | description                                                        |
|---------------|---------------|-------------------------------------------|--------------------------------------------------------------------|
| `SV_HOSTNAME` | string        | Quake 3: Arena server hosted on zerops.io | Server hostname.                                                   |
| `MOTD`        | string        | Welcome to zerops.io Quake 3: Arena       | Message of the day.                                                |
| `ENABLE_BOTS` | bool (1 or 0) | 1                                         | Enables bots on the server.                                        |
| `MIN_PLAYERS` | int           | 8                                         | Minimum players on server, remaining spots will be filled by bots. |
| `MAX_PLAYERS` | int           | 16                                        | Maximum players on server.                                         |
| `TIME_LIMT`   | int           | 10                                        | Maximum round time.                                                |
| `FRAG_LIMIT`  | int           | 30                                        | Target frag count, after which is change of round.                 |

<br/>

If you have any troubles running the server or whatever, join our [Discord server](https://discord.gg/WDvCZ54) and ask there :) **Enjoy!**
