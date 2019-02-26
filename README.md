# Teeworlds Server Startup Scripts (1.0.0)
Startup scripts for the Teeworlds game software - uses the "screen" command to manage session. This also restarts the Teeworlds server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/TeeworldsStartup) - [Official Forum](https://gameplayer.club/phpBB3/viewforum.php?f=8)  - [Official Download Area](https://gameplayer.club/index.php/downloads/category/13-teeworlds)

---

These start up the Teeworlds server at boot time with a "screen" process.

1. Copy **teeworlds** into **/etc/init.d** - make sure it is executable
2. Copy **startteeworlds** into **/root/twserver** - make sure it is executable
4. Run "**systemctl enable teeworlds**" (only needed once, will stick)
5. Run "**systemctl start teeworlds**" - starts Teeworlds without restarting the server

When you want to view the Teeworlds console, just enter "**screen -r**" in your shell.

To disconnect from the Teeworlds console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/teeworlds/nostart**". To reenable it type "**rm /root/teeworlds/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
