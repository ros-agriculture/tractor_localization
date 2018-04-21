

Reference material for setting up transforms for your robot.

http://www.ros.org/reps/rep-0105.html - Coordinate Frames for Mobile Platforms

An example of the different TF's on your robot:
http://wiki.ros.org/hector_slam/Tutorials/SettingUpForYourRobot#Overview


We use the center of rotation for the base_link position.  This is for Ackermann style vehicles:

  > http://docs.ros.org/api/ackermann_msgs/html/msg/AckermannDrive.html
  >
  > All are measured at the vehicle's
  > center of rotation, **typically the center of the rear axle**.
  

The Static Transform Publisher node is used to publish the measurements:
http://wiki.ros.org/tf#static_transform_publisher

Please refer to the ROS documentation for standard measurements: 
  http://www.ros.org/reps/rep-0103.html 
  
  Example for your launch file.  Base link to Odom published at 10 hz:
  ``` XML
      <node pkg="tf" type="static_transform_publisher" 
        name="base_link_transform" 
        args="0 0 0 0 0 0 base_link odom 10" />
  ```
  These are the measurements in **meters** for your sensors (x y z yaw pitch roll)  x forward y left z up  
