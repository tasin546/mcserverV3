# mcserverV3 — Minecraft Cloud Server Toolkit

Host your own **Java** or **Bedrock** Minecraft Server for free using **Google Cloud Shell**. Works on `Ubuntu/Debian` based Linux. **No credit card required**.

## Features
- Java servers: Vanilla, Paper, Forge, Fabric, Sponge, Spigot, BungeeCord
- Bedrock servers: Vanilla, Nukkit, PocketMine-MP
- Auto-restart on crash with crash counter
- Automatic EULA acceptance
- Playit.gg tunnel for public access (no port forwarding)
- Keep-alive heartbeat to prevent Cloud Shell timeout
- World backup system with automatic cleanup
- Java 17 & Java 21 support

## Quick Start
```bash
git clone https://github.com/Tasin546/mcserverV3
cd mcserverV3
chmod +x *
./install
./startserver
```

## Commands
| Command | Description |
|---|---|
| `./install` | Install Java/Bedrock server + dependencies |
| `./startserver` | Start the server, tunnel, and keep-alive |
| `./stopserver` | Stop everything gracefully |
| `./backup` | Create a timestamped world backup |
| `./update` | Update project scripts (keeps server data) |
| `./uninstall` | Delete server files |

## Connecting to Your Server
After starting the server, run `screen -r playit` to see your tunnel URL. Click the **Claim URL**, create a free playit.gg account, add a Minecraft tunnel, and use the generated `auto.playit.gg` address to connect.

## Useful Screen Commands
| Command | Description |
|---|---|
| `screen -r server` | View server console |
| `screen -r playit` | View tunnel/IP info |
| `screen -r afk` | View keep-alive heartbeat |
| `Ctrl+A` then `D` | Detach from screen session |

## Customizing Server Variables
Edit the files in `JavaInstallScripts/` or `BedrockInstallScripts/`. Only modify between these markers:
```
# -- EDIT HERE | DO NOT EDIT ABOVE -- #
YOUR_VARIABLES=here
# -- EDIT HERE | DO NOT EDIT BELOW -- #
```

## Limitations
- **50 hours/week** — Google Cloud Shell has a weekly quota
- **No dedicated IP** — you must use playit.gg for public access
- **Browser must stay open** — Cloud Shell terminates idle sessions (the built-in heartbeat helps extend this)

## Links
- [Submit Issues](https://github.com/Tasin546/mcserverV3/issues)

## Credits
> Project Creator & Maintainer: *[Tasin546](https://github.com/Tasin546)*

> Original Concept: *[LordOfWizard](https://github.com/lordofwizard)*
