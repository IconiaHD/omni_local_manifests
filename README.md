omni_local_manifests
====================

Local manifests for building Omnirom for Acer A200

How to use :
------------

Put the files 'a200_device' & 'a200_vendor' into '.repo/local_manifests/' directory as follow :

mkdir -p .repo/local_manifests

curl https://raw.github.com/IconiaHD/omni_local_manifests/master/a200_device > .repo/local_manifests/a200_device.xml
curl https://raw.github.com/IconiaHD/omni_local_manifests/master/a200_vendor > .repo/local_manifests/a200_vendor.xml

and use 'repo sync' command to fetch specifics A200 components
