# FAQs Citadel

---

### Terminology

GUI = Graphical user interface (Web browser)

CLI = Command line interface (terminal)

---

### Quickstart

<details><summary></summary>

</details>

<details>
  <summary>I have installed Citadel OS, what now?</summary>
  
  - Open any browser from any of your devices
  
  - Type in the address bar `citadel.local` OR your node IP address - for help see **Need your node's IP address?**
  
  - type in your password
  
  - enjoy Citadel
  
</details>

<details>
   <summary>Need your node's IP address?</summary>
  
  - Install Angry IP Scanner [here](https://angryip.org/)
  
  - Open Angry IP Scanner and press "Start"
  
  - Identify the IP address of your node looking at "Hostname" and "Ping" (keep in mind that Ethernet has lower ping than Wifi)
</details>

---

### Access your node
  
  You can access your node via GUI (Graphical User Interface) or via SSH (Terminal) from your home-network.
  If you want to access your node from a remote place (not from within your home-network) you can also do     so either via GUI on Tor-Browser or via SSH.
 
 <details><summary>via GUI in home network</summary>

  - Open any browser
  
  -  Type in the address bar `citadel.local` OR your node IP address - for help see **Need your node's IP address?**
  
  - type your password
</details>

 <details><summary>via GUI with Tor</summary>

  - Open the Tor browser
  
  -  Type in the address bar the .onion address of your node that you can find under "Settings"
  
  - type your password
</details>
 
 <details> <summary>via SSH</summary>
  
  - Open the Terminal on any device you want to use for SSH into your node

  - write `ssh -t [account_name]@[ip_address]`

  - replacing `[account_name]` with the name of the account you used when installing Citadel

  - replacing `[ip_address]` with the IP address of your node - for help see **Need your node's IP              address?
 </details>

---

### View logs

<details><summary>via GUI</summary>
  - Open any Browser and log in into to your node - for help see **How to access your node?**
  
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

