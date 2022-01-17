# ros2-training
## install ros2 foxy on Ubuntu 20.04
minimal install
25g drive space
install viritalbox tools
  might need to install tools twice
setup shared clipboard on virtialbox
sudo apt-get install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
add ssh key to know hosts (ssh to it and save it)
  look into playbook to do this later on...


# install tools
https://code.visualstudio.com/docs/?dv=linux64_deb
vs code extensions:
  c/c++
  CMake
  Python

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








