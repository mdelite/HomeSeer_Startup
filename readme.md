# HS4 Linux Startup and Shutdown

My attempt to get my HS4 system to automatically startup when my machine starts.

Started with this post from the HomeSeer forums [HS3 Linux startup and shutdown](https://forums.homeseer.com/forum/homeseer-products-services/system-software-controllers/hs3-hs3pro-software/hs3-hs3pro-discussion/79355-hs3-linux-startup-and-shutdown).

## Notes:
The spelling out shutdown part is because for whatever reason, homeseer wont take
the characters that fast. The sleeps make it work. You can use screen -r -S HomeSeer
from another ssh shell to see it happen. Note the ^D is created by hitting Ctrl-V
then Enter in vi in insert mode. It is not just a ^ and D

The script should be created in /etc/init.d as root. It gets added to auto startup
by issuing the command `sudo update-rc.d homeseer defaults`. After that Homeseer
will start and stop automatically when the server starts and stops

command line Use:
```
sudo service homeseer start
sudo service homeseer stop
sudo service homeseer restart
```

Connect to the console at any time by issuing
```
sudo screen -r -S HomeSeer
```
^[https://forums.homeseer.com/forum/homeseer-products-services/system-software-controllers/hs3-hs3pro-software/hs3-hs3pro-discussion/79355-hs3-linux-startup-and-shutdown?p=766560#post766560]
