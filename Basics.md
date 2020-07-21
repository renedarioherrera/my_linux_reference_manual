# Basics


## System updates


### Check for updates


       update (apt-get(8))
           update is used to download package information from all configured
           sources. Other commands operate on this data to e.g. perform
           package upgrades or search in and display details about all
           packages available for installation.


```
$ sudo apt update
```


### Upgrade Software


       upgrade (apt-get(8))
           upgrade is used to install available upgrades of all packages
           currently installed on the system from the sources configured via
           sources.list(5). New packages will be installed if required to
           satisfy dependencies, but existing packages will never be removed.
           If an upgrade for a package requires the remove of an installed
           package the upgrade for this package isn't performed.



```
$ sudo apt upgrade
```


### Clean 


       autoclean (and the auto-clean alias since 1.1)
           Like clean, autoclean clears out the local repository of retrieved
           package files. The difference is that it only removes package files
           that can no longer be downloaded, and are largely useless. This
           allows a cache to be maintained over a long period without it
           growing out of control. The configuration option
           APT::Clean-Installed will prevent installed packages from being
           erased if it is set to off.



```
sudo apt autoclean
```


### Remove 


      autoremove (apt-get(8))
           autoremove is used to remove packages that were automatically
           installed to satisfy dependencies for other packages and are now no
           longer needed as dependencies changed or the package(s) needing
           them were removed in the meantime.

           You should check that the list does not include applications you
           have grown to like even though they were once installed just as a
           dependency of another package. You can mark such a package as
           manually installed by using apt-mark(8). Packages which you have
           installed explicitly via install are also never proposed for
           automatic removal.


```
sudo apt autoremove
```
