# Discord & Steam Phishing URLs

This repository contains a sorted [scam-urls.txt](https://raw.githubusercontent.com/Dogino/Discord-Phishing-URLs/main/scam-urls.txt) file of known phishing links used on Discord. 
Scammers and userbots might use those links for stealing tokens, passwords, IP addresses and much more. Please check below the list of the currently known scams on Discord.
**Be careful NOT to open those links or download any file for ANY reason** unless you understand the risks and know what you are doing.

You may want to check [this domain list](https://raw.githubusercontent.com/Dogino/Discord-Phishing-URLs/main/official-domains.txt) and compare those links to see if they are legit or not.

## Purpose of this repository
- Comparing domains to see if they are used for phishing
- Checking which scams are currently used by userbots and what to do in case you got scammed
- Blocking those URLs from loading completely in your home network using [Pi-Hole](https://github.com/pi-hole/pi-hole) adlists (use [this file](https://raw.githubusercontent.com/Dogino/Discord-Phishing-URLs/main/pihole-phishing-adlist.txt) as adlist to block them and make sure gravity is costantly updated)
- Phades, a Discord bot which deletes and bans users who post these links

## Adding & Removing links
**If you find a new domain which is not included in this list, please open a issue or a pull request.** You do not need to update the pihole file if you don't want to, it will get updated with the daily domain update with your link. Some of these domains are found using a simple regex in a big list of daily registered domains, some false positives might be included in this list and if your domain or a domain which is not used for phishing is included, please submit a issue so I can remove it accordingly. I do not have plans to remove old phishing urls even if they don't work anymore and temporary/free domain hostings/link shorteners won't be added to the list (such as replit, github.io, altervista, bit.ly, goo.gl etc)

## Phades
Phades is a Discord bot which takes action upon detecting one of these links. It currently has two functions of automoderation, one used for phishing urls from this list and one for shorteners, server admins can toggle if to kick or ban users when a phishing link is detected and nothing/kick/ban users when a shortener link is detected. Phades doesn't store any data about servers or users besides your server id used for configurations of the two options above. A rewrite is in progress to convert every command to slash due to Discord's deadline on August, when the slash rewrite will be completed the entire source of Phades will be made public and people can deploy their own hosted instance without using mine. You might want to run !help to see all available commands, phades only responds to server admins/founders in the current state. You can invite Phades by [clicking this link](https://discord.com/api/oauth2/authorize?client_id=926211335946137771&permissions=1529210072134&scope=bot%20applications.commands). 

## Currently known scams and what to do 

> Free nitro X months from (enter brand here, eg: steam, discord, steelseries)

**Mostly used in server text channels**, they use edited Discord names with a fake embed to make it look real or lowercase letters (eg: dlscord where the `l` it's a L in lowercase or dscords.tld) in the attempt that people won't notice the mispelled domain, they could also use some randomly generated slashes after such as "nitro from dlscord.tld/free-nitro" and when this page is opened it usually asks to login to "claim" such nitro. They also attempt to ping `@everyone` or `@here`.
**If you logged in through this url**, your login token (which allows you to stay logged in) is probably in their hands and they will spam the same thing with your name in all your servers and friends, **please change your Discord password (and email password if it's the same) as soon as possible.**

> Hypesquad is recruiting... | Join the discord moderation team... | Join the events | Your account is in danger...

**Those are usually sent in private messages** by userbots faking system messages with names like "Hype Squad Events" or "Moderation Team", Discord has recently blocked people from adding "Discord" to their own name but they usually use hypesquad or similar to those. 
It's the same as above, some fake domain like "join-the-hypesquad-team.tld" where you are supposed to login, if your browser is updated you should get a warning message before opening such page, so keep your system and your browser updated to detect those links even before they can load. **If you logged in those sites with your QR code or with your login data, again, change your passwords. If you wonder how a REAL Discord message looks like, they have a "SYSTEM" icon next to their name**, like bots have "BOT", please look at [this Discord support page](https://support.discord.com/hc/en-us/articles/360036118732-Discord-System-Messages) which shows you how it looks.

> Can we talk for a moment? I recently reported you on (steam) due to a mistake...

**This is a Steam phishing attempt, usually sent in private messages**, they claim to be like steam moderators or middlemans/steam staff and they need you to verify your identity or something like that, please remember that Steam Support won't contact you on Discord, they will mail you using their official domain name, scammers will probably give you some fake steam page (like steamncommunity.tld) where you are supposed to login or to trade skins/steam items in order to "avoid" getting banned, once again, Steam won't ever contact you on Discord if you did something, so don't bother opening those sites.

> I am a game/software developer and I want you to test my game/software...

**This is usually sent in private messages** and you should avoid it before it's too late. They ask you to "playtest" their little game of around 100mb which could be a demo/alpha/anything linking you some website which shows some image with a download link (you can check that the download link is usually from Discord itself, like `discord.com/0000/0000/game.zip` because they use their servers or Discord to host the malware). **This is a wide-spreaded RAT which will download your Discord login data, token, IP addresses, 2FA backup codes** (including your current one so they can relogin in your account), **browser passwords and cookies** (which allows them to login to 2FA protected pages without using 2FA at all) **and even extensions passwords** (such as MetaMask for cryptocurrency), they can also install cryptominers in your pc and/or other types of malware. **Those programs/fakegames are NOT detectable from your antimalware software** and they usually use a node.js or a unity packed file with some random game name asking you to open it for testing, if you really want to test it, please defend yourself using a offline virtual machine and a VPN in your main system, **do not** open these files in your main system for any reason.
**If it happened that you opened one of those, your entire system ~~might be~~  is compromised and most of your data, browser history and passwords, credit card details, discord login and 2fa tokens might be in their hands already, change ALL your password of ALL your accounts in ALL websites as soon as possible using another machine** (smartphone, another computer etc) and if you had your credit card details saved, contact your bank and block your card asap. Please avoid opening unknown .exes and .zips sent by random people on Discord. 
Please note that some browsers (eg: Chrome) costantly synchronize your changed passwords and history automatically across all devices upon opening if you are logged with their accounts (for Chrome, it's your Google account), uninstall your browser before changing your details or your changes will be sent to them or format your PC using a USB drive with a fresh, non-compromised Windows image.

There might be new ones and scammers always try to change their methods to avoid getting easily detected, if you got scammed or they tried to scam you, please send a ticket to Discord support (using [this link](https://dis.gd/contact)) to get those bots banned and potential accounts saved. You can avoid all of those scams with just common sense, no one gives you free stuff, no Steam/otherbrand support will contact you on Discord and you shouldn't be opening random mispelled discord/steam websites or download random .exes from the internet.

## Credits

 - [discord-scam-links](https://github.com/BuildBot42/discord-scam-links) by BuildBot42
 - [scam-links](https://github.com/DevSpen/scam-links) by DevSpen
 - [discord-phishing-links](https://github.com/nikolaischunk/discord-phishing-links) by nikolaischunk
 - WHOIS Newly registered domains
 - Other sources from public servers and contributors