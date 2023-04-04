robot_localization
==================

robot_localization is a package of nonlinear state estimation nodes. The package was developed by Charles River Analytics, Inc.

Please see documentation here: http://docs.ros.org/noetic/api/robot_localization/html/index.html

EDIT for ReZoom: Include paths in `/include/navsat_conversions.h` and `/include/navsat_transform.h` is changed from the original repository (This was done to bypass an error). Make sure you edit them for your system. 

This repository requires both the apt installation of `GeographicLib` and an installation from source in your home repository (This will be the include path you have to change as mentioned above). 

Run `sudo apt-get install libgeographic-dev ros-noetic-geographic-msgs` to get the apt installation (if not done already). Next, install from source, go to your desired directory (I keep it in my home) and run:
```
git clone git://git.code.sourceforge.net/p/geographiclib/code ./geographiclib
cd geographiclib
mkdir build && cd build
cmake .. && make
sudo make install
```

You should be able to build this package without any errors after this.
