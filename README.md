# Jetson-Nano-Ubuntu20.04-ROS-Realsense
* Ubuntu 20.04
https://qengineering.eu/install-ubuntu-20.04-on-jetson-nano.html
https://github.com/Qengineering/Jetson-Nano-Ubuntu-20-image
https://qengineering.eu/install-ubuntu-20.04-on-jetson-nano.html#upgrade


* Setup VNC and Resolution
https://developer.nvidia.com/embedded/learn/tutorials/vnc-setup
(only last half) https://github.com/overclock98/Jetson_Nano_true_Headless_setup_without_hdmi_display 
	
6-Enabling Automatic Login (otherwise cant start from ssh): steps
    Open the custom.conf file in the Nano editor
$ sudo nano /etc/gdm3/custom.conf
    commented-out these lines and replace user1 with your username (mine is nano)
AutomaticLoginEnable = true
AutomaticLogin = nano

* Fix Lavapipe
@Qengineering I ran into the same issue and deleted directory /usr/share/vulkan/icd.d and it went away (NVidia config is in /etc/vulkan/icd.d btw.). Looks like they removed it in Jetpack as well (don't see it in NVidia's 18.04).

* Intel Realsense + pyrealsense2 lib
https://jstar0525.tistory.com/97
Errr OpenSSL: 
sudo apt-get install -y build-essential libssl-dev uuid-dev cmake libcurl4-openssl-dev pkg-config
Thanks,
sojohans

* PyTorch
https://qengineering.eu/install-pytorch-on-jetson-nano.html

* Pil
sudo apt-get install python3-pil

* Pygame
https://forums.developer.nvidia.com/t/install-pygame-on-jetson-nano/83731/7

For them who might find it interesting, some updates to install pygame 2.0.0 on Jetpack 4.5.1, Python3 on Jetson Nano:

    sudo apt-get install python3-dev libsdl2-image-dev libsdl2-mixer-dev libsdl2-ttf-dev libsdl2-dev libsmpeg-dev python3-numpy subversion libportmidi-dev ffmpeg libswscale-dev libavformat-dev libavcodec-dev libfreetype6-dev
    sudo python3 -m pip install pygame==2.0.0

An ‘import pygame’ is executed successfully.
regards, Peter

* Error OpenCV:
https://automaticaddison.com/how-to-install-opencv-4-5-on-nvidia-jetson-nano/
