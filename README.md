# rust-game

A rust-admin game server. The recommended machine configuration is 4 cores and 16GB of RAM for a 100 player server.

## Create a new server

### install SteamCMD
enable support for 32-bit architecture 
```bash
sudo add-apt-repository multiverse
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install steamcmd
``` 
the game is installed in the `~/.local/share/Steam` directory, so the rust game is installed in `~/.local/share/Steam/rust`

### configure the start script

here [start paramate](https://developer.valvesoftware.com/wiki/Rust_Dedicated_Server) is the parameter list for the rust server.

```bash
# example
./RustDedicated -batchmode +server.port 777 +rcon.port 9999 +rcon.password "YourRconPassword" +rcon.web 1 +server.tickrate 10 +server.hostname	"Your Server Name" +server.identity	"my_server_identity" +server.maxplayers	50 +server.worldsize	3000  +server.saveinterval	3000 -silent-crashes -logfile 2>&1 
```


### Reference

[linux server install for rust game](https://wiki.facepunch.com/rust/Creating-a-server#linuxserverinstallation)