**List of DebianDog-Squeeze fixes found after 29.08.2015:**

**1.** The installer scripts bugs fixing created new problem and the last two versions removed from the repository. 
Recommended to make sure you have this version on your system by reinstalling this package: [debdoginstallscripts_1.0.5_i386-squeeze.deb](http://smokey01.com/saintless/DebianDog-Squeeze/Packages/Included/debdoginstallscripts_1.0.5_i386-squeeze.deb)

Or by running in terminal:
```
sudo apt-get update
sudo apt-get remove debdoginstallscripts
sudo apt-get install debdoginstallscripts
```

**2.** Some fixes from Fred for fixdepinstall (install deb and dependencies right click option).
[More information read here.](http://murga-linux.com/puppy/viewtopic.php?p=871384#871384)
Install fixed version from the link above or from terminal:
```
sudo apt-get update
sudo apt-get install fixdepinstall
```

**3.** Fix for squashfs module loading scripts from Fred. [More information read here.](http://murga-linux.com/puppy/viewtopic.php?p=878996#878996)
```
sudo apt-get update
sudo apt-get install sfsload portablesfs-loadsfs-fuse
```

**4.** Small fix for frisbee. [More information read here.](http://murga-linux.com/puppy/viewtopic.php?p=883158&sid=3588429564754e676ce49df134d930a8#883158)
```
sudo apt-get update
sudo apt-get install frisbee
```

**5.** Small fix for apt2sfs. [More information read here.](http://murga-linux.com/puppy/viewtopic.php?p=885536&sid=e09b92e591e85bcc4632168abdb32e5b#885536)
```
sudo apt-get update
sudo apt-get install apt2sfs
```

**6.** With porteus-boot and only when using save on exit code upgrading libc6 could create some issues. More information and workarownd read [here](http://murga-linux.com/puppy/viewtopic.php?p=889934&sid=00f59036fe7b1df6f8bc7168fe1df597#889934) and the fix [here.](http://murga-linux.com/puppy/viewtopic.php?p=890342&sid=00f59036fe7b1df6f8bc7168fe1df597#890342)
Install this package to fix the problem:
```
sudo apt-get update
sudo apt-get install porteusbootscripts

```

**7.** Debian Squeeze main, contrib and non-free repositories are available only in Debian archive repository now.
Run these commands in terminal to fix the problem:
```
sudo apt-get update
sudo apt-get install debdog-repo-updater
sudo apt-get update

```
Or change the line in /etc/apt/sources.list to archive.debian.org (installing debdog-repo-updater package will do the same change):
```
deb http://archive.debian.org/debian/ squeeze main contrib non-free
#deb http://ftp.debian.org/debian/ squeeze main contrib non-free
```
