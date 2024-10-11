# Zerops x Quake 3

Do you know feeling of nostalgia, when you want to play some old first-person shooters, but don't want to spend time configuring the server?
Well here's your solution, quick and easy way to start you own Quake 3: Arena server and play with your friends.

[LinuxGSM](https://linuxgsm.com/) used to deploy this game server. For more advanced configuration look [here](https://linuxgsm.com/servers/q3server/).

<br/>

## Deploy on Zerops

<br/>

You need to enable IPv4 connectivity, follow these extra steps in GUI:

- Projects > `quake3-server`
    - IP Addresses & Public Routing Overview > (Activate) Unique IPv4 address
    - Services > `q3server` > Public access & internal ports > Public Access through IP Addresses > Setup up the first
      access through IPv4

You can change server hostname and motd by changing following environment variables in `zerops-import.yml` or `zerops.yml`.

| key           | default                                   | description         |
|---------------|-------------------------------------------|---------------------|
| `SV_HOSTNAME` | Quake 3: Arena server hosted on zerops.io | Server hostname.    |
| `MOTD`        | Welcome to zerops.io Quake 3: Arena       | Message of the day. |

<br/>

If you have any troubles running the server or whatever, join our [Discord server](https://discord.gg/WDvCZ54) and ask there :) **Enjoy!**