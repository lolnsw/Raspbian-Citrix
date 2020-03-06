# Raspbian-Citrix

Install Citrix debian package:
==================================
sudo dpkg -i /path/to/deb/file.deb

Citrix certificates error fix:
======================
sudo ln -s /usr/share/ca-certificates/mozilla/* /opt/Citrix/ICAClient/keystore/cacerts

Citrix full screen
=====================
sudo apt-get install icewm <br/>
Edit "/etc/xdg/lxsession/LXDE/desktop.conf" and "/etc/xdg/lxsession/LXDE-pi/desktop.conf":<br/>
In both files earch for:<br>
[Session]<br/>
window_manager=openbox-lxde-pi<br/>
and in both files change it to:<br/>
[Session]<br/>
window_manager=icewm<br/>
<br/>
remove icewm bar:<br/>
vi /usr/share/icewm/preferences<br/>
ShowTaskBar=0<br/>

Numlock on boot
=================
sudo apt-get install numlockx<br/>
sudo vi /etc/X11/xinit/xinitrc <br/>
if [ -x /usr/bin/numlockx ];<br/>
then<br/>
    /usr/bin/numlockx on<br/>
fi<br/>

