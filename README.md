# Apple2js Startup Scripts (1.0.0)
Startup scripts for the Apple2js Apple 8-bit emulator - uses the "screen" command to manage a session. This also restarts the apple2js process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/Apple2js-Startup) - [Official Forum](https://appleii.retro-os.live/index.php/forum/our-apple-e-web-emulator-tools)  - [Official Download Area](https://appleii.retro-os.live/index.php/downloads/category/23-our-server-tools)

---
These start up the apple2js server at boot time with a "screen" process.

1. Copy **apple2js** into **/home/apple2/bin** - make sure it is executable
2. Copy **emuindex** into **/home/apple2/bin** - make sure it is executable
3. Copy **startapple2js** into **/home/apple2/apple2js** - make sure it is executable
4. Put **@reboot /home/apple2/bin/apple2js start** into your crontab

When you want to view the Apple2js console, just enter "**screen -r**" in your shell.

To disconnect from the Apple2js console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

If you want to turn off the server respawning type "**touch /home/apple2/apple2js/nostart**". To reenable it type "**rm /home/apple2/apple2js/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
