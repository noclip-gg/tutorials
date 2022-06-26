# Store Linking
<img src='https://i.imgur.com/UtQ8Vd2.png' alt='Noclip Logo' width=64px>

Linking your Noclip Store to your Garry's Mod server will automatically allow users to receive their packages.

**Requirements:**
- You must have stripe linked to your noclip account.
- Access to the Store settings (Inside your Noclip Dashboard)
- FTP File Access to upload the Gmod Files

Picture step by step: [here]().

## Download the Store File [here](https://github.com/noclip-gg/noclip-donation-gmod).

Once you have downloaded the noclip-donation-gmod, you will need to upload it via FileZilla or WinSCP.
Once uploaded via FTP you can now config the addon, please go to the following file locaion (noclip-donation-gmod-1.1.2\lua\noclip_store\config).

## Setting up the sv_config file.

First you will need your community API key, please go to your dashboard and press general settings, then press Reset API key,
then scroll all the way down to the bottom, copy then paste your API key in the sv_config file (NoClip.Store.Config.APIKey = "ABC-123-XYZ")

Then you will need the URL to your community. Ensure there is no trailing "/", copy your community URL and replace "https://mycommunity.noclip.me" 
with your own URL. 

Next you will need your "ServerID". to find this please go to https://mycommunity.noclip.me/admin/servers, make sure you have created a server,
when you have created your server you will see the "ID" please copy and past your server ID here NoClip.Store.Config.ServerID = "YOURID"

The next few steps are completly your choice, please make sure not to set the Store.Config.Check too less as this may cause lag.

##Setting up the sh_language file and cl_config.

These two files do not require any setup but you can edit anything here to match your country's language or to change the colour of the donation notification.


---

## Support

If you encounter any problems with setting up or configuring Discord sign in get some assistance please ask in our Discord [here](https://physgun.com/discord).