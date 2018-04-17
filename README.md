<pre>

# tractor_localization
Robot_Localization with GPS and IMU

# Install dependencies
# GPS

sudo apt-get install -y ros-kinetic-nmea-comms \
 ros-kinetic-nmea-msgs \
 ros-kinetic-nmea-navsat-driver \
 ros-kinetic-geographic-info \
 ros-kinetic-geographic-msgs \
 ros-kinetic-unique-id \
 ros-kinetic-unique-identifier


# Razor IMU
sudo apt-get install -y ros-kinetic-razor-imu-9dof

# Robot Localization
sudo apt-get install -y ros-kinetic-robot-localization

Setup TF measurements in the /launch file

http://wiki.ros.org/tf#static_transform_publisher 
These are the measurements for your sensors (x y z yaw pitch roll)  
Where x forward y left z up  http://www.ros.org/reps/rep-0103.html
</pre>
