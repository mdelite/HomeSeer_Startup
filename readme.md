# HS4 Linux Startup and Shutdown

My attempt to get my HS4 system to automatically startup when my machine starts.
This is currently working on my Linux box running Ubuntu 22.04.4 LTS. 

## Instructions
The `homeseer.service` is wanting HomeSeer to be installed in the `/opt/HomeSeer/`
directory. If installed in another location, update the paths in the file.
1. Copy the systemd service file `homeseer.service` to the `/etc/systemd/system/` directory.
2. Run the following to start the service and checkt that it is running.
```
sudo systemctl enable homeseer
sudo systemctl start homeseer
sudo systemctl status homeseer
```
