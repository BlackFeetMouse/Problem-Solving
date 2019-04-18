## AR Environment Setup 

### Problem Description: At first I run cmake and design the project on Xcode for AR exercise-1, but when I run the program it fed back error message "OpenCV 4.x+ requires enabled C++11 support" (I also tried Clion but got same error)

**Solution**
Using Clion, CLion -> Preferences -> Build, Execution, Development -> CMake -> add ```-DCMAKE_CXX_FLAGS="-std=c++11``` to CMake Options.

[Add flag on CLion](https://www.jetbrains.com/help/clion/how-to-switch-compilers-in-clion.html)

[Error Solution Website](https://github.com/BVLC/caffe/issues/6358)

## iMac Poweroff randomly

### Problem Description: The iMac at Lab Shut down randomly starting from 4/11/2019.

**Solution**
* Change cable
* Release stastic electricity
* Reset [NVRAM](https://support.apple.com/en-us/HT204063) (memory that Mac uses to store certain settings and access them quickly)
* Reset [SMC](https://support.apple.com/en-us/HT201295)
