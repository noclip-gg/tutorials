# Adding a domain to Noclip
<img src='https://i.imgur.com/l4QcLFe.png' alt='Noclip Logo' width=64px>

**Requirements:**
- You **must** own a domain or be ready or purchase a domain through a registrar.
- You need to either have [Noclip Rainbow](https://noclip.me/upgrade) or be a [Noclip partner](https://noclip.me/partners).

## Purchasing a domain

You will need to purchase a domain through a registrar like [Namecheap](https://namecheap.pxf.io/noclip/) or [PorkBun](https://porkbun.com/).
<br>
**DO NOT USE GODADDY**

*GoDaddy has a fundimental flaw in their DNS configurations.*

If you already own a domain you can go ahead and use that for Noclip.

---

## Configuring your forum

You must claim your domain to your forum.

You can do this by going to your **forums dashboard**, under the **settings** tab.
If you can't  find the field for setting your vanity domain, scroll down.
Your vanity domain **can** be a subdomain, like `forum.example.com`.

<img src='https://i.imgur.com/jD9lJDp.png' alt='Screenshot of Vanity Domain setting' width=550px>

---

## Domain Configuration

There are 2 ways to add a domain to Noclip, you can either change your Nameservers via your domain control panel or your can create a CNAME record via your DNS settings.

This guide assumes you're not using Cloudflare, if you are follow the additional instructions below.

### CNAME

Via your DNS control panel you can set records specifying your domain to point to Noclip, this is a CNAME record. You can optionally read about CNAME records [here](https://www.cloudflare.com/en-gb/learning/dns/dns-records/dns-cname-record/).

*If you're using GoDaddy this **may** not work*

Log into your domain registars panel, you will find a tab called something similar to `DNS`.
<br>
For Namecheap it is under `Account -> Dashboard -> Manage -> Advanced DNS`.
<br>
For PorkBun it is under `Domain Management -> Details -> DNS Records`.

Once you're here you will need to create the record for the (sub-)domain that you'd like, the route/host will be `@` and the target/address will be `noclip-bohbc.ondigitalocean.app.`

Each registrars panel may differ from anothers, please make sure to look around and check their support articles. 

### Nameservers

Via your domains control panel, you can change the nameservers of your domain.
This allows Noclip to fully control your domain and add and remove [records](https://www.cloudflare.com/learning/dns/dns-records/).
<br/>
**YOU WILL NOT BE ABLE TO CONTROL INDIVIDUAL RECORDS | NOCLIP WILL HAVE FULL CONTROL**

1. Navigate to your domains control panel. (Namecheap's website for example)
2. Locate the section which manages your nameservers.
3. **Replace** your existing nameservers with the ones provided below.
4. Wait for your domain to be added by Noclip staff. (This may take some time)
5. Enjoy 🙂

```
ns1.digitalocean.com
ns2.digitalocean.com
ns3.digitalocean.com
```
^ `ns` referrs to nameserver, you can find more information about nameservers [here](https://www.cloudflare.com/en-gb/learning/dns/dns-records/dns-ns-record/).

# Troubleshooting & More Info

## Support

Support is provided by the community in the Noclip Discord server. You can join that [here](https://physgun.com/discord)
<br>
Make sure to accept the rules, you won't be able to chat if you don't.

## Cloudflare

If you are using Cloudflare for your domain for DDOS protection you **MUST** disable Cloudflare's protection for the DNS record Noclip will be accesible via.

You can do this by switching `Proxy status` to the disabled position.
<img src='https://i.imgur.com/Ykj3wXj.png' alt='Cloudflare DNS Dashboard with Noclip CNAME' width=550px>

## GoDaddy

If the CNAME for Noclip doesn't work and you're using GoDaddy as your registrar this is due to GoDaddy's DNS settings. To get around this you can use the Nameserver method or use an external DNS provider like Cloudflare.
