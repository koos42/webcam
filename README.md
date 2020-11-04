# webcam
Use a raspberry pi with a camera as a webcam for meetings, by piping the camera output to the HDMI port. It's up to you to get an HDMI to USB dongle, and plug it into your computer. The webcam waits until it has a network connection, and attempts to put its IP address on the local network as an overlay on the video, so you can more easily ssh into your raspberry pi, if that's something you're into.

## requirements
Raspberry pi with camera module. The install assumes you've setup the webcam and enabled it using raspi-config, this assumes you're using "raspian", and it's up to date.

## install
### install webcam command
1. `sudo mv webcam /usr/bin/webcam`
2. `sudo chown root:root /usr/bin/webcam`
3. `sudo chmod 755 /usr/bin/webcam`

### install webcam service
1. `sudo mv webcam.service /etc/systemd/system/webcam.service`
2. `sudo chown root:root /etc/systemd/system/webcam.service`
3. `sudo chmod 644 /etc/systemd/system/webcam.service`

### enable the service
`sudo systemctrl enable webcam.service`

## TODOs:
- [ ] makefile for easier install
- [ ] publish stl/vectors for cutting out "enclosure"
- [ ] add buttons and means of turning camera on/off
- [ ] add light to show when camera is on
- [ ] add button to cycle through video effects and camera options
