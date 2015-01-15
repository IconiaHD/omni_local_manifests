omni_local_manifests
====================

Local manifests for building Omnirom for Acer A200 (Lollipop update)

How to use :
------------

Yes all the source code is available on Github.

These are the steps to build this rom.

- Install a suitable OS. You can use a virtual machine running Ubuntu 12.04 64-bit, or a physical one : both are supported.

- Prepare the system, do steps 1, 2 and 5 of this guide, to configure your development machine :

http://forum.xda-developers.com/showthread.php?t=1762641
Tutorial To Compile JB on Ubuntu - xda-developers

WARNING : To have success when building ROMs from repository, it's essential tu use SUN Java-6 JRE (not 1.7, or later)
If you don't use this one, you'll have unpredictable errors, like C header files malformed.

It's recommanded to have a PATH pointing the right Java JRE at first position, in your environment !

If you wish to install the right JRE on your Ubuntu 64 bits machine, you can download & execute this :

    http://domi.dambrain.free.fr/Android/Acer_A200/KitKat/jdk-6u38-linux-x64.bin


Then run these commands:
------------------------

mkdir YOUR_ WORKING_DIR

cd YOUR_WORKING_DIR

repo init -u git://github.com/omnirom/android.git -b android-5.0

mkdir .repo/local_manifests

curl https://raw.github.com/IconiaHD/omni_local_manifests/omni-5.X/a200_device.xml > .repo/local_manifests/a200_device.xml

curl https://raw.github.com/IconiaHD/omni_local_manifests/omni-5.X/a200_kernel.xml > .repo/local_manifests/a200_kernel.xml

curl https://raw.github.com/IconiaHD/omni_local_manifests/omni-5.X/a200_vendor.xml > .repo/local_manifests/a200_vendor.xml

repo sync



The sync will take a while and download something like 15 GB of source code.

Finally build the rom with these commands:
------------------------------------------

 source build/envsetup.sh

 brunch a200



If all goes well this will create a zip file into 'out' folder, that can be flashed on the tablet!

