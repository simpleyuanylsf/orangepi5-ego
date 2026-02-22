```
git clone https://gitee.com/wx_338946ef59/Fast-Drone-250.git
```

#安装ros

```
wget http://fishros.com/install -O fishros && . fishros
```

#安装realsense

```
sudo apt-get install ros-noetic-realsense2-*
```

#安装mavros

```
sudo apt-get install ros-noetic-mavros ros-noetic-mavros-extras
cd /opt/ros/noetic/lib/mavros
sudo ./install_geographiclib_datasets.sh
```

#编译库 安装依赖

```
cd Fast-Drone-250
unzip 3rd_party.zip
cd glog
sudo chmod +x ./autogen.sh 
./autogen.sh 
```

```
sudo chmod +x ./configure 
./configure 
```

```
make 
sudo make install
```

```
sudo apt-get install liblapack-dev libsuitesparse-dev libcxsparse3 libgflags-dev libgoogle-glog-dev libgtest-dev
```

```
cd ..
cd ceres
mkdir build
cd build
cmake ..
```

```
sudo make -j4
sudo make install
```

```
sudo apt-get install ros-noetic-ddynamic-reconfigure
```

#编译源代码

```
cd ~/Fast-Drone-250
catkin_make
source devel/setup.bash
```

