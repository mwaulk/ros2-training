# ros2-training
## install ros2 foxy on Ubuntu 20.04
minimal install
25g drive space
<!-- sudo apt update
sudo apt upgrade
sudo apt install build-essential gcc make perl dkms python3 python3-pip python-is-python3 -->
install viritalbox tools
might need to install tools twice
setup shared clipboard on virtialbox
sudo apt-get install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
add ssh key to know hosts (ssh to it and save it)
  look into playbook to do this later on...

# install tools
<!-- sudo apt install build-essential gcc make perl dkms python3 python3-pip python-is-python3 terminator python3-colcon-common-extensions python3-colcon-ros -->
https://code.visualstudio.com/docs/?dv=linux64_deb
vs code extensions:
  c/c++
  CMake
  Python

# install ros2
<!-- https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html
pip3 install argcomplete
edit .bashrc
  source /opt/ros/foxy/setup.bash
  export BLINKA_FT232H=1
  source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash
sudo reboot -->

# install code for FT232H breakout
<!-- #sudo apt-get install libusb-1.0
sudo vi /etc/udev/rules.d/11-ftdi.rules 
SUBSYSTEM=="usb", ATTR{idVendor}=="0403", ATTR{idProduct}=="6001", GROUP="plugdev", MODE="0666"
SUBSYSTEM=="usb", ATTR{idVendor}=="0403", ATTR{idProduct}=="6011", GROUP="plugdev", MODE="0666"
SUBSYSTEM=="usb", ATTR{idVendor}=="0403", ATTR{idProduct}=="6010", GROUP="plugdev", MODE="0666"
SUBSYSTEM=="usb", ATTR{idVendor}=="0403", ATTR{idProduct}=="6014", GROUP="plugdev", MODE="0666"
SUBSYSTEM=="usb", ATTR{idVendor}=="0403", ATTR{idProduct}=="6015", GROUP="plugdev", MODE="0666"
sudo udevadm control --reload-rules
sudo udevadm trigger
sudo adduser $USER plugdev
log user out and back in
pip3 install pyftdi
pip3 install adafruit-blinka
export BLINKA_FT232H=1
python3
from pyftdi.ftdi import Ftdi
Ftdi().open_from_url('ftdi:///?') -->

# MCP2221A
<!-- sudo apt-get install libusb-1.0 libudev-dev
sudo vi /etc/udev/rules.d/99-mcp2221.rules
SUBSYSTEM=="usb", ATTRS{idVendor}=="04d8", ATTR{idProduct}=="00dd", MODE="0666"
sudo udevadm control --reload-rules
sudo udevadm trigger
pip3 install hidapi
sudo rmmod hid_mcp2221 -->
## these two command do not work. Need to figure out how to do this in current os
<!-- #blacklist hid_mcp2221
#sudo update-initramfs -u
pip3 install adafruit-blinka
export BLINKA_MCP2221=1 -->

# hidapi - this is required by MCP2221A
<!-- sudo apt-get install python-dev libusb-1.0-0-dev libudev-dev -->
# not sure why this is needed
# sudo pip install --upgrade setuptools
<!-- sudo pip install hidapi -->




# bno055 driver
apt search linux-headers-$(uname -r)
sudo apt install libi2c-dev
cd ~/ros2_ws/src
https://github.com/bdholt1/ros2_bno055_sensor


# create ros2 workspace
mkdir ros2_ws
mkdir ros2_ws/src
cd ..
concon build
cd
vi .bashrc
source ~/ros2-training/ros2_ws/install/setup.sh

# create ros2 package python
ros2 pkg create my_py_pkg --build-type ament_python








