# Discord OAuth
<img src='https://i.imgur.com/UtQ8Vd2.png' alt='Noclip Logo' width=64px>

Enabling Discord OAuth (Sign in with Discord) will allow people to log into your forum with their Discord account without having to use Steam.

**Requirements:**
- Understanding what OAuth is
- A Discord 'Application'
- Discord application Client ID & Client Secret.

Picture step by step: [here](https://imgur.com/a/Yffi3Fk).

## Create a Discord Application

Applications on Discord allow developers to interact with Discord without using the UI, to setup Discord OAuth for your forum you will need to make a Discord application. That can be done [here](https://discord.com/developers/applications).

Sign into Discord if you are not, once at the developer landing page click on the `Applications` tab if you aren't already on it, in the top right you will find a button with `New Application`, click it and create your application with a desired name. People will be able to see this name when they sign in, choose wisely. (You can change it later)

## OAuth ID & Secret

On your Discord application configuration page navigate to OAuth2; under the general tab you will need to note down the Client ID and the Client Secret.

## OAuth settings on Noclip

Login to your forums on your administrator account, navigate to your Dashbord, then to `Settings` then `Social`, at the bottom of the page there will be forms for you to fill in your Discord applications OAuth information. Fill it in with the Client ID and Client Secret you got from Discord.

Go back to the Discord application portal then enter (yourdomain/oauth/discord/callback) in the Redirect area under the OAuth2 tab and save.

---

## Support

If you encounter any problems with setting up or configuring Discord sign in get some assistance please ask in our Discord [here](https://discord.gg/xtrSJ4fD2z).
