---
title: Create Instance
parent: Instance
grand_parent: Setup
nav_order: 1
layout: default
---

# Create Instance
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

{: .attention}
You need to create an account before creating a CedMod instance. Following the [account creation guide](), if you haven't already

---

## Choose Server

When creating, a CedMod instance, you have to choose a linking discord server.
Only servers that have the CedMod bot on it will be shown,
add it
using [this link](https://discord.com/oauth2/authorize?client_id=749684016550248490&permissions=536870912&scope=bot).
After adding the bot, you can then select the server on the panel and proceed with the instance creation.

{: .note}
After adding the bot to your server, it can take a few minutes until the server shows up on the panel

## Set Panel Location

After selecting your server, you will be prompted with an option to choose a panel location.
Here you should choose the location that is the nearest to your server's location/your playerbase.

You have the choice between **Germany** and **Canada**.
We would encourage you to use the following location,
depending on your server location:

<dl>
  <dt>Europe</dt>
  <dd>Germany Panel</dd>
  <dt>America</dt>
  <dd>Canada Panel</dd>
  <dt>Asia</dt>
  <dd>Germany Panel</dd>
</dl>

## Basic Setup

Now you need to choose your top domain. 
Currently, CedMod only supports the `yourinstance.cmod.app` domain.

{: .deprecated }
If you want to use a custom domain, contact CedMod support.

{: .new }
You are now able to go to the custom domains page after creating your instance to use a custom domain

After defining the top domain, you need to name your instance.
This name will replace the `yourinstance` part in the top domain and be displayed on the instance's panel page as well.

Then you'll be asked to set the default admin role.
Make sure that you select the correct role as panel administrator access is really powerful.

At last, you can disable/enable certain features.
You can activate them later after the setup if you change your mind.

- [x] Enable AntiVPN?
- [x] Disable IP Bans for Ip addresses used for Cloud Gaming
- [x] Log Panel Actions

| Feature                          | Definition                                                                                                                                                                                                                                                                                                                                |
|:---------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AntiVPN                          | The AntiVpn will prevent anyone who is not allowlisted from it from joining your server. The AntiVpn can protect against people trying to evade bans using Alt accounts and VPNS. Players who get kicked for using Cloud gaming or have to use a vpn for legitimate reasons can request a whitelist using the link in the kick message.   |
| Disable IP Bans for Cloud gaming | When this option is enabled, Players that use Cloud gaming will not get kicked when there is an Ip ban on the ip of that cloud gaming server. As cloud gaming Ip addresses are shared, commonly players may get kicked if ip bans are enabled for cloud gaming. It is recommended to leave this option on for the best player experience. |
| Log Panel Actions                | If enabled, Bans, Mutes and Warns will be logged to the webhooks defined below.                                                                                                                                                                                                                                                           |

## Webhook Setup

Here you can define the channels specific types of logs are sent to. 
The options are explained below the category, 
you can also set all logs to a single channel

| Webhook               | Definition                                                                                        |
|:----------------------|:--------------------------------------------------------------------------------------------------|
| `WebhookGeneralUse`   | All logs that do not belong to a specific category will be sent here, e.g., important information |
| `WebhookBans`         | All analogs will be sent here                                                                     |
| `WebhookBanJoinKicks` | All ban join kicks will be sent here (players that are banned trying to join the server)          |
| `WebhookUnbans`       | All unbans will be sent here                                                                      |
| `WebhookWarns`        | All warns will be sent here                                                                       |
| `WebhookMutes`        | All mutes will be sent here                                                                       |
| `WebhookUnmutes`      | All unmutes will be sent here                                                                     |
| `WebhookAntiVpn`      | All AntiVPN kicks will be sent here (if feature is enabled)                                       |

## Link Instance to Server

{: .attention}
DO NOT share your activation key with anyon

After creating the instance, you need to paste a command similar to this into your server console.
Make sure to replace `<cedmod_activation_key>` with your key

```console
$~ setupcedmod <cedmod_activation_key>
```