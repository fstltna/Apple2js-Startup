# Apple2js Startup Scripts (1.0.0)
Startup scripts for the Apple2js Apple 8-bit emulator - uses the "screen" command to manage a session. This also restarts the apple2js process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/CoffeeStartup) - [Official Forum](https://pocketmud.com/index.php/forum/server-utils)  - [Official Download Area](https://pocketmud.com/index.php/download-upload/category/4-servers)
![Coffee MUD Sample Screen](https://pocketmud.com/coffee_mud.png)

---
These start up the apple2js server at boot time with a "screen" process.

1. Copy **apple2js** into **/home/apple2/bin** - make sure it is executable
2. Copy **startapple2js** into **/var/www/html/apple2js** - make sure it is executable
4. Put **@reboot /home/apple2/bin/apple2js start** into your crontab

When you want to view the Apple2js console, just enter "**screen -r**" in your shell.

To disconnect from the Apple2js console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

If you want to turn off the server respawning type "**touch /var/www/html/apple2js/nostart**". To reenable it type "**rm /var/www/html/apple2js/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
