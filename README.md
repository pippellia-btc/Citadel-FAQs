# FAQs Citadel

---

### Terminology

GUI = Graphical user interface - in this case a web browser

CLI = Command line interface - in this case a terminal

---

- **I have installed Citadel OS, what now?**
  
  - Open any browser from any of your devices
    
  - Type in the address bar `citadel.local` OR your node IP address - for help see **Need your node's IP address?**
    
  - type in your password
    
  - enjoy Citadel
    
- **Need your node's IP address?**
  
  - Install Angry IP Scanner [here](https://angryip.org/)
    
  - Open Angry IP Scanner and press "Start"
    
  - Identify the IP address of your node looking at "Hostname" and "Ping" (keep in mind that Ethernet has lower ping than Wifi)
    
- **Want to SSH into your node?**
  
  - Open the Terminal on any device you want to use for SSH into your node
    
  - write `ssh [account_name]@[ip_address]`
    
    - replacing `[account_name]` with the name of the account you used when installing Citadel
      
    - replacing `[ip_address]` with the IP address of your node - for help see **Need your node's IP address?**
      
- **How to access your node (GUI)?**
  
  - Open any browser
    
  - Type in the address bar `citadel.local` OR your node IP address - for help see **Need your node's IP address?**
    
  - type your password
    
- **Want to shutdown your node? (GUI)**
  
  - Open any browser
    
  - Type in the address bar `citadel.local` OR your node IP address - for help see **Need your node's IP address?**
    
  - type your password
    
  - go to "Settings"
    
  - press "Shutdown"
    
- **Want to restart your node? (GUI)**
  
  - Open any browser
    
  - Type in the address bar `citadel.local` OR your node IP address - for help see **Need your node's IP address?**
    
  - type your password
    
  - go to "Settings"
    
  - press "Restart"
    
- **Want to update Citadel (GUI) ?**
  
  - Open any Browser and log in into to your node - for help see **How to access your node (GUI)?**
    
  - go to "Settings"
    
  - press "Check for updates", then "Install Now" if there are any updates
    
- **Want to update Citadel (CLI) ?**
  
  - SSH into your node - for help see **Want to SSH into your node?**
    
  - write `sudo ~/citadel/scripts/update/update --repo runcitadel/core#v0.2.2`
    
- **Need logs for troubleshooting (GUI)?**
  
  - Open any Browser and log in into to your node - for help see **How to access your node?**
    
  - go to "Settings"
    
  - under "Troubleshooting" press "Start"
    
- **Need logs for troubleshooting (CLI)?**
  
  - SSH into your node - for help see **Want to SSH into your node?**
    
  - write `sudo ~/citadel/scripts/debug --upload --no-tor`
    
- **Want to start Citadel (CLI)?**
  
  - SSH into your node - for help see **Want to SSH into your node?**
    
  - write `sudo ~/citadel/scripts/start`
    
- **Want to stop Citadel from (CLI)?**
  
  - SSH into your node - for help see **Want to SSH into your node?**
    
  - write `sudo ~/citadel/scripts/stop`
    
- **Want to install an app (CLI)?**
  
  - SSH into your node - for help see **Want to SSH into your node?**
    
  - write `sudo ~/citadel/scripts/app install [app_name]` replacing `[app_name]` with the name of the app you wish to install e.g. `fulcrum`
    
- **Want to do a full reset (BACKUP EVERYTHING FIRST) ?**
  
  - Backup every data that is important on a secure device different from your node.
    
  - SSH into your node - for help see **Want to SSH into your node?**
    
  - write `sudo ~/citadel/scripts/stop && sudo rm -rf ~/citadel/app-data/* && sudo rm -f ~/citadel/statuses/configured ~/citadel/db/user.json ~/citadel/db/citadel-seed/seed && sudo ~/citadel/scripts/start && sudo ~/citadel/scripts/start`
    

---

**Did you find these FAQs helpful and valuable? You can give value back!**

**In ⌛ Time, 🎨 Talent and 🧡 Sats!** 

Help us share Citadel with friends and family and consider sending some sats our way on our [Geyser page](https://geyser.fund/project/runcitadel). Thank you :pray:

Need additional help? Take a look below 👇

---

- **Need additional help (GUI)?**
  
  - generate logs for Troubleshooting GUI - for help see **Need logs for troubleshooting (GUI)?**
    
  - Press "Download logs"
    
  - Join the [Telegram group of Citadel](https://t.me/runcitadel/1), describe in detail what happened and attach the logs file.
    
  - have patience :)
    We are a small team, but we are trying our best to get back to you asap!
    
- **Need additional help (CLI)?**
  
  - generate logs for Troubleshooting CLI - for help see **Need logs for troubleshooting (CLI)?**
    
  - copy the sharable link you get
    
  - Join the [Telegram group of Citadel](https://t.me/runcitadel/1), describe in detail what happened and paste the logs-link
    
  - have patience :)
    We are a small team, but we are trying our best to get back to you asap!
    

- **How to restart a Docker Container**
  `sudo docker restart lnd-service-1`
