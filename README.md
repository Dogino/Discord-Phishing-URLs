# Discord Phishing URLs

This repo contains txt files of discord phishing urls.

## Credits

 - [discord-scam-links](https://github.com/BuildBot42/discord-scam-links) by BuildBot42
 - [scam-links](https://github.com/DevSpen/scam-links) by DevSpen
 - Other sources from public servers and contributors.
 
## Adding links
I'll add links when I find new ones, feel free to PR if you want to contribute. I'm not planning to remove those links even if they won't work anymore, I doubt Discord/Steam will buy those fake domains for official purposes.

## Usage
You can add my bot for automatically ban those links and there is also a [Pi-Hole](https://github.com/pi-hole/pi-hole) file which you can use in order to block those malicious domains with your Pi-Hole DNS.

## Discord Blacklist bot
I made a discord blacklist bot which bans users who send those domains. You can invite the bot using [this link](https://discord.com/api/oauth2/authorize?client_id=926211335946137771&permissions=1531156229190&scope=bot%20applications.commands), it will **not** collect any data from messages nor users. If you find new domains that the bot doesn't detect, please let me know so I can add them in the blacklist file, thank you!

When a link containing a domain from the message is detected, the bot will warn in chat for 10 seconds and bans the user. You can unban users from discord -> server settings -> user management section -> bans. If you have feedback it's appreciated.

The invite url has only the permissions to ban users but not administrator, don't use administrator since it's not required. If you want to esclude a channel from the bot's monitoring, in the channel settings just block the bot's view to it.