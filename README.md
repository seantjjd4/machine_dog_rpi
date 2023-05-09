# machine_dog_rpi

machine_dog_rpi is a system built base on ROS2 (humble) structure for **Raspberry Pi 3 Model B**.

## Installation (ROS2)

### Linux [Ubuntu 22.04.2 LTS (Jammy Jellyfish)]

#### Set locale
Make sure you have a locale which supports UTF-8.
```bash
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```
#### Add the ROS 2 apt repository
You will need to add the ROS 2 apt repository to your system.

+ Ensure that the Ubuntu Universe repository is enabled.
```bash
sudo apt install software-properties-common
sudo add-apt-repository universe
```

+ Add the ROS 2 GPG key with apt.
```bash
$ sudo apt update && sudo apt install curl -y
$ sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```

+ Then add the repository to your sources list.
```bash
$ echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```

#### Install ROS2 and development tools
```bash
$ sudo apt update # update your apt repo caches
$ sudo apt install ros-humble-desktop
```

```bash
# get to the top level of the workspace
# inside directory => src/
cd machine_dog_ws/

# build
```
