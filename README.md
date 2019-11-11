# CppND-Program-a-Concurrent-Traffic-Simulation-L3

Overview  
[![Alt text](https://img.youtube.com/vi/vfNXDebmZIM/0.jpg)](https://youtu.be/vfNXDebmZIM)

Code Walkthrough
Note: we recommend playing the video below full-screen so you will be able to see the code.  
[![Alt text](https://img.youtube.com/vi/w4L17HaT2Xk/0.jpg)](https://youtu.be/w4L17HaT2Xk)

Project Tasks
- **Task L3.1** : In class WaitingVehicles, safeguard all accesses to the private members _vehicles and _promises with an appropriate locking mechanism, that will not cause a deadlock situation where access to the resources is accidentally blocked.
- **Task L2.2** : Add a static mutex to the base class TrafficObject (called _mtxCout) and properly instantiate it in the source file. This mutex will be used in the next task to protect standard-out.
- **Task L2.3** : In method Intersection::addVehicleToQueue and in Vehicle::drive() ensure that the text output locks the console as a shared resource. Use the mutex _mtxCout you have added to the base class TrafficObject in the previous task. Make sure that in between the two calls to std::cout at the beginning and at the end of addVehicleToQueue the lock is not held.

Build Instructions
To run this code using a Udacity workspace, you will need to use the virtual desktop. In the desktop you can use Terminator or the terminal in Visual Studio Code.

Once in the virtual desktop, to compile and run the code, create a build directory and use cmake and make as follows:

root@a9ad274128c4:/home/workspace/L1_Project# mkdir build  
root@a9ad274128c4:/home/workspace/L1_Project# cd build  
root@a9ad274128c4:/home/workspace/L1_Project/build# cmake ..  
root@a9ad274128c4:/home/workspace/L1_Project/build# make  
root@a9ad274128c4:/home/workspace/L1_Project/build# ./traffic_simulation  


## Dependencies for Running Locally
* cmake >= 2.8
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* OpenCV >= 4.1
  * The OpenCV 4.1.0 source code can be found [here](https://github.com/opencv/opencv/tree/4.1.0)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./traffic_simulation`.
