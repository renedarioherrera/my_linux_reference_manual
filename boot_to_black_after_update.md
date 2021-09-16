# Did Nvidia update break my display?

If, after an `apt update && apt upgrade` the system boots to a black screen it may be that the Nvidia graphics driver update broke the display.

The solution may be to:

1. Open a terminal either by SSH into system or first `CTRL+ALT+F1` then `CTRL+ALT+F2`
2. then update and upgrade system packages `apt update && apt upgrade`
3. purge Nvidia then install the appropriate driver, for example: `apt purge nvidia*:any && apt install nvidia-driver-465`
4. reboot `sudo reboot`
