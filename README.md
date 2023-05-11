# FAQs Citadel

---

#### Terminology

_GUI = Graphical user interface_

_CLI = Command line interface_

---

### Quickstart

<details>
  <summary>I have installed Citadel OS, what now?</summary>
  
  - Open any browser from any of your devices
  
  - Type in the address bar `citadel.local` OR your node IP address - for help see [Need your node's IP address?](#quickstart)
  
  - type in your password
  
  - enjoy Citadel
  
</details>

<details>
   <summary>Need your node's IP address?</summary>
  
  - Install Angry IP Scanner [here](https://angryip.org/)
  
  - Open Angry IP Scanner and press "Start"
  
  - Identify the IP address of your node looking at `Hostname` and `Ping`
  (keep in mind that Ethernet has lower ping than Wifi)
</details>

---

### Access your node
  
  You can access your node via _GUI (Graphical User Interface)_ or via _SSH (Terminal)_ from your home-network.
  If you want to access your node from a remote place (not from within your home-network) you can also do     so either via GUI on Tor Browser or via SSH.
 
 <details><summary>via GUI - home network</summary>

  - Open any browser
  
  -  Type in the address bar `citadel.local` OR your node IP address - for help see [Need your node's IP address?](#quickstart)
  
  - type your password
</details>

 <details><summary>via GUI - Tor</summary>

  - Open the Tor browser
  
  - Type in the address bar the `.onion address` of your node that you can find under "Settings"
  
  - type your password
</details>
 
 <details> <summary>via SSH</summary>
  
  - Open the Terminal on any device you want to use for SSH into your node

  - write `ssh -t [account_name]@[ip_address]`

      - replacing `[account_name]` with the name of the account you used when installing Citadel

      - replacing `[ip_address]` with the IP address of your node - for help see [Need your node's IP   address?](#quickstart)
 </details>

---

### View logs

<details><summary>via GUI</summary>
  
  - Open any Browser and log in into to your node - for help see **Access your node**
  
  - go to "Settings"
  
  - under "Troubleshooting" press "Start"
</details>

<details><summary>via CLI</summary>

  - SSH into your node - for help see **Access your node**
  
  - for detailed logs write `sudo ~/citadel/scripts/debug --upload --no-tor`
  
  There are several other options for citadel logs:
  - `cat ~/citadel/logs/karen.log`
  - `cat ~/citadel/logs/status-monitor.log`
  - `cat ~/citadel/logs/backup-monitor.log`
  
  And there are also application-specific logs.
  
  - `sudo docker logs --tail=100 lnbits-main-lnd-1`
  - `sudo docker logs --tail=100 lnd-service-1`
  - `sudo docker logs --tail=100 lnd-backup-1`
  - `sudo docker logs --tail=100 manager`
</details>

---

### Start, Stopping, Updating

### Citadel
<details><summary>via GUI</summary>
  
- Open any Browser and log in into to your node - for help see **Access your node**
  
- go to "Settings"
  
- _Updating_: click "Check for updates", then "Install Now" if there are any updates

- _Stopping_: click "Shutdown" or "Restart"

</details>

<details><summary>via CLI</summary>
  
- SSH into your node - for help see **Access your node**
  
- _Start_: write `sudo ~/citadel/scripts/start`

- _Stop_: write `sudo ~/citadel/scripts/stop`
  
- _Update_: write `sudo ~/citadel/scripts/update/update --repo runcitadel/core#v0.2.2`
Make sure to replace the version with the one you want to install.
Note that it is recommended to update via GUI.
</details>

### Your apps

<details><summary>via GUI</summary>
  
- Open any Browser and log in into to your node - for help see **Access your node**
  
- _Installation_: Go to "App Store" where you can find all compatible Apps for your Version of Citadel. Choose the app you want and click install and
copy the passwort shown in the right upper corner to open the app. All installed apps are also accessible from the menue "Apps"

- _Updating_: Go to "Apps" and click "Update"
  
- _Deinstallation_: Go to "Apps" and click "Edit", choose the App to deinstall and click "Uninstall"

</details>

<details><summary>via CLI</summary>
  
  As an example we took LNbits here but it works like this for all others, too.
  
- SSH into your node - for help see **Access your node**
  
- _Start_: write `sudo ~/citadel/scripts/app start lnbits`

- _Stop_: write `sudo ~/citadel/scripts/app stop lnbits`
  
- _Update_: write `sudo ~/citadel/scripts/app stop lnbits && sudo ~/citadel/scripts/app update && sudo ~/citadel/scripts/app start lnbits`
  
</details>

---

### Backup

Citadel does an automatic backup of your channel. Additionally you can run a backup, whenever you like by SSHing into your node and typing

`I HAVE ABSOLUTELY NO IDEA.COM`

---

### Restore

We hope you did the backup! Having done that we can move on 🔥

write `sudo ~/citadel/scripts/stop && sudo rm -rf ~/citadel/app-data/* && sudo rm -f ~/citadel/statuses/configured ~/citadel/db/user.json ~/citadel/db/citadel-seed/seed && sudo ~/citadel/scripts/start && sudo ~/citadel/scripts/start`

---

**Did you find these FAQs helpful and valuable? You can give value back!**

**In ⌛ Time, 🎨 Talent and 🧡 Sats!** 

Help us share Citadel with friends and family and consider sending some sats our way on our [Geyser page](https://geyser.fund/project/runcitadel). Thank you :pray:

---

### Need additional help?

<details><summary>via GUI</summary>

- generate logs - for help see **view logs**
  
- Press "Download logs"
  
- Join the [Telegram group of Citadel](https://t.me/runcitadel/1), describe in detail what happened and attach the logs file.
  
- have patience :)
  We are a small team, but we are trying our best to get back to you asap!
</details>

<details><summary>via CLI</summary>

- generate logs - for help see **view logs**
  
- copy the sharable link you get
  
- Join the [Telegram group of Citadel](https://t.me/runcitadel/1), describe in detail what happened and paste the logs's link
  
- have patience :)
  We are a small team, but we are trying our best to get back to you asap!
</details>
