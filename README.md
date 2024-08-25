Ubuntu/Debian and derivatives


Make sure you have Wayland Session enabled (Ubuntu 22.04+)




sudo apt install curl ca-certificates -y



curl https://repo.waydro.id | sudo bash

sudo apt install waydroid -y

NixOS community has a wiki page for WayDroid:



Copy
sudo waydroid container start
And in a new terminal tab, start the waydroid session (without sudo):

Copy
waydroid session start
After that starts and you see "Android with user 0 is ready", it is safe to launch an app from the applications menu, or

Launch Waydroid In Full-Screen Mode:
(This can be run while Waydroid is running, or used to start it in full-screen mode)

Copy
waydroid show-full-ui
Launch Waydroid In Multi-Window Mode:
First we need to set the property while a Waydroid session is running:

Copy
waydroid prop set persist.waydroid.multi_windows true
After that, we can restart the session:

Copy
waydroid session stop
Then we are ready to launch an app, and it will start in multi-window mode

Reinstalling Waydroid
Sometimes things don't go as planned and you need to remove it all and start over. To do that, follow the steps below:

First, make sure you have stopped the session and containers:

Copy
waydroid session stop
sudo waydroid container stop
Then it is safe to remove Waydroid. For example, on debian or ubuntu:

Copy
sudo apt remove waydroid
