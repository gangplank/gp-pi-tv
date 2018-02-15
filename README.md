# gp-pi-tv
Pi Zero W Image for TVs at Gangplank Locations to Display information about the location on the TVs

To Setup for your location please follow the steps below:

1. Burn Image on to SD card
2. With card in your computer go to the boot directory/partition
3. Within the boot directory, Right-Click > New > Text Document and rename the document to wpa_supplicant.conf - Make sure that you change the file extention from .txt to .conf
4. Add the following to the file (update network if you had a heroin problem)

```
country=US
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
network={
    ssid="gangplank"
    psk="walktheplank"
}
```
5. Enable SSH but placing a blank file name ssh (no extension) in the boot directory/partition
6. Put SD Card in Pi Zero W and connect to TV.
7. SSH into the Pi with username pi and password mofos2010
8. Change password with the passwd command
9. If you want to change the pages that are being rotated:
  - Run vi /home/pi/kiosk.sh
  - Edit the line below # Run Chromium and open tabs with the urls you want in each tab (separated by a space)
  - If you want to change rotation timing change the sleep 15 command to however many seconds you want in the same file
10. sudo reboot your pi

If you have any questions contact refriedchicken in the #queen-creek Slack channel.


DOWNLOAD THE INITIAL IMAGE HERE: https://s3-us-west-2.amazonaws.com/refriedchicken/gangplank/pi-images/gp-tv-pi.img
