# utils_pkg

This is an utils repo support some useful ros packages on melodic.

utils_pkg repo including:
* apriltags_ros
* realsense-ros for librealsense 2.36.0
* vision_opencv
* geometry2

## ROS Distro Support

|         | Melodic | Noetic  |
|:-------:|:-------:|:-------:|
| branch | [`melodic`](https://github.com/kuolunwang/utils_pkg/tree/melodic) | [`noetic`](https://github.com/kuolunwang/utils_pkg/tree/noetic) |
| Status | supported | supported |

## Clone this repo

```
    git clone --recursive git@github.com:kuolunwang/utils_pkg.git
```

## Notice

**If you want to use vision_opencv and tf in python3, you need compiling before catkin_make your workspeace.**

You can add below command on the script.

```
    catkin_make --pkg vision_opencv -C [your workspace] \
                -DCMAKE_BUILD_TYPE=Release \
                -DPYTHON_EXECUTABLE=/usr/bin/python3 \
                -DPYTHON_INCLUDE_DIR=/usr/include/python3.6m \
                -DPYTHON_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython3.6m.so

    catkin_make --pkg geometry2 -C [your workspace] \
                --cmake-args \
                -DCMAKE_BUILD_TYPE=Release \
                -DPYTHON_EXECUTABLE=/usr/bin/python3 \
                -DPYTHON_INCLUDE_DIR=/usr/include/python3.6m \
                -DPYTHON_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython3.6m.so
```