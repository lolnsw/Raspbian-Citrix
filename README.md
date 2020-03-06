# Raspbian-Citrix

Install Citrix debian package:
==================================
sudo dpkg -i /path/to/deb/file.deb

Citrix certificates error fix:
======================
sudo ln -s /usr/share/ca-certificates/mozilla/* /opt/Citrix/ICAClient/keystore/cacerts

Citrix full screen
=====================
sudo apt-get install icewm
Edit "/etc/xdg/lxsession/LXDE/desktop.conf" and "/etc/xdg/lxsession/LXDE-pi/desktop.conf":<br>
In both files earch for:<br>
[Session]
window_manager=openbox-lxde-pi
and in both files change it to:
[Session]
window_manager=icewm

remove icewm bar:
vi /usr/share/icewm/preferences
ShowTaskBar=0

Numlock on boot
=================
sudo apt-get install numlockx
sudo vi /etc/X11/xinit/xinitrc 
if [ -x /usr/bin/numlockx ];
then
    /usr/bin/numlockx on
fi

