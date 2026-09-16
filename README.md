Babel update for AREDN 4.26.7.0
===

Below is a link to download a new verison of Babel suitable for installing on AREDN 4.26.7.0. This new version includes a single bug fix to remove a potential maximum 4MB memory leak.

*HOWEVER* before you install this package please following the steps below to see if you should. In many cases this update will not effect how your node behaves or is not suitable for your device. There is no need to update a node with this fix if it is already working.

Should I install?
--

1. Does you node have only 64M of memory?
   If you have more memory then this fix will do nothing. Yes you're wasting 4M of memory, but you node is under no memory pressure so there will be no operational difference. **If you have more than 64M of memory don't install this.**
2. Is your node part of the *ath79* family?
   If you don't know you can check the supported device list which includes this information (see https://github.com/aredn/aredn/blob/main/SUPPORTED_DEVICES.md). In fact there is only one 64M node which isn't - the "LDF 5 ac" - contact me if you have that node and need this fix as the package below is not for you. **If your node isn't *ath79* don't install this.**
3. Is your node running out of memory? If you're node isn't running out of memory then this fix wont change anything for you. The memory leak is a *maxiumum* of 4MB. **If you're not running out of memory now this fix won't change anything so don't install this.**

Installing
--

If you still need to install this fix then download the single Babel package found here:

https://github.com/kn6plv/babel-update-4.26.7.0/raw/refs/heads/main/babel-1.13.1-r2.apk

Rather than installing entirely new firmware, we are just install this fix. You can find instructions on how to do this in the documentation here:

https://docs.arednmesh.org/en/latest/arednGettingStarted/node_admin.html#package-settings

This replaces the current Babel program with the new one. The installed package count will not change - if it was zero before it will be zero after this. Now reboot your node and you're done.

This memory fix, and a few others which save more memory, will be part of the next AREDN release.

Thanks - The AREDN Team
