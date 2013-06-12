LightDM Webkit Greeter Ubuntu Theme
===========================

This is a LightDM webkit greeter theme for Ubuntu. Based on [LightDM-Webkit-MacOSX-Theme](http://github.com/Wattos/LightDM-Webkit-MacOSX-Theme)

Installation Instructions
-------------------------
You will need lightdm as your login manager and the lightdm-webkit-greeter from the Ubuntu Software Repositories. You need to make the webkit greeter the default greeter. This is done by editing the lightdm configuration under:

<pre>
/etc/lightdm/lightdm.conf
</pre>

and changing the greeter-session value to lightdm-webkit-greeter. lightdm.conf should have:

<pre>
[SeatDefaults]
greeter-session=lightdm-webkit-greeter
allow-guest=false
</pre>

If you would like to enable the guest account, just change the allow-guest value from "false" to true, so it would look like this:

<pre>
[SeatDefaults]
greeter-session=lightdm-webkit-greeter
allow-guest=true
</pre>

The second step is to install the actual theme. This is done by copying the files of this repository into the following location:

<pre>
/usr/share/lightdm-webkit/themes/ubuntu
</pre>

Finally, change the /etc/lightdm/lightdm-webkit-greeter.conf file to contain the following line:

<pre>
webkit-theme=ubuntu
</pre>

Now you can reboot and enjoy the new theme.
