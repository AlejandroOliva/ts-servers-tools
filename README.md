# SCS Truck Simulator Server Tools

The intention of this project is to facilitate the management of SCS Dedicated Servers for American Truck Simulator and Euro Truck Simulator 2 on Linux platform in a simple way.

## SCS Dedicated Servers
It is assumed that you have already installed SteamCMD and ETS2 Dedicated Server and/or ATS Dedicated Server from the Steam application cmd manager.
If not, please refer to the documentation for both processes.
-  [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD)
-  [SCSSoft Dedicated Server](https://modding.scssoft.com/wiki/Documentation/Tools/Dedicated_Server)


## Where to place these files
You can download the files, unzip them and put them directly in the `/usr/local/bin/` folder.
This way, you will have instant access to the new commands.
It is strongly recommended not to clone the repository in this path because administrator permissions are required.

Alternatively, you can download or clone this repository to the user's home folder (`/home/{user}/`), or wherever you feel most comfortable.
Choosing this method, the next step will be to add the folder in the `PATH` environment variable.
1. Open a terminal on your operating system.
2. Identify your login configuration file. You can use one of the following files: .bash_profile, .bashrc, .zshrc, or .profile. You can verify which one exists on your system by using the ls -a ~ command.
3. Edit the login configuration file you identified in the previous step. You can use a text editor in the terminal, such as nano or vi, to open the file. For example, if you use nano, you can run nano .bash_profile.
4. Add the following line to the file, replacing /path/to/ts-servers-tools with the full path to the "ts-servers-tools" directory:  
`export PATH="/path/to/ts-servers-tools:$PATH"`
5. Save the changes and close the configuration file.
6. Restart the terminal for the changes to take effect.

Once the installation of the scripts is complete, make sure you have the necessary configuration files described in the SCSSoft Dedicated Servers documentation to start the servers.

Note that if you want to run a server for each of the versions (ATS / ETS2) you will need to configure different ports for each one.  
You will also need to enable the ports as described in the SCSSoft Documentation.

## Command List

### `ats-server` / `ets2-server`

Start ATS or ETS2 server

### `ats-server-stop` / `ets2-server-stop`

Stop all running ATS or ETS2 servers

### `ats-server-restart` / `ets2-server-restart`

Stops all running ATS or ETS2 servers and starts a new server for the same game

### `ats-server-log` / `ets2-server-log`

Displays ATS or ETS2 server log 

### `ts-servers`

Start 2 servers, one for each game (`ats-server` + `ets2-server`)

### `ts-servers-stop`

Stops all running ATS & ETS2 servers (`ats-server-stop` + `ets2-server-stop`)

### `ts-servers-restart`

Stops all running ATS & ETS2 servers and starts a new server for each game (`ats-server-stop` + `ets2-server-stop`, then `ats-server` + `ets2-server`)