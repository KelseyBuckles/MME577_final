

# ROS package: MME577_final

This package includes 3 subpackages: kelsey_topics, kelsey_actions, kelsey_services, along with their corresponding launch files.
kelsey_topics contains message and topic publisher and subscriber nodes under the names message_publisher.py, message_subscriber.py, topic_publisher.py, and topic_subscriber.py which allows nodes to communicate by publishing (speaking), and subscribing (listening).
This package also includes a custom message description--Complex.msg--for messages containing real and imaginary numbers.
kelsey_actions is where subpackages that ask nodes to actually DO things would live. Currently, the only action is Timer.action, which waits a certain amount of time, keeps track of the total actual wait time and total number of feedback updates sent, and prints time elapsed and time remaining as feedback on each time step (note that this is different from a service since it provides feedback during execution).
kelsey_services includes subpackages where one node provides a function to the other nodes. Currently the only service file in there is WordCount.srv, which counts words.

## Requirements

This system will work on Linux based machines running Ubuntu Bionic 18.04.4, ROS Melodic Morenia, and Python 2.

## Installation and configuration

Once your machine is setup with ROS Melodic Morenia, Python 2, and git, fork and clone this repository from a terminal window in your machine, into a ROS workspace's src directory. Then, navigate to your workspace root, and build the workspace using `catkin_make`. Then, source the workspace using `source devel/setup.bash`. You can generally launch the desired subpackage using the format `roslaunch <name of subpackage> <launch file name>`. For eample, to launch the kelsey_actions subpackage, use `roslaunch kelsey_actions fancy_action.launch`. An exception is the services subpackage which will need a message to count the words of. This launch command will be of the form `roslaunch kelsey_services fancy_service.launch <enter your own message here>`. Additionally, kelsey_topics has 2 launch files that need to be launched, so the command to launch that subpackage will be `roslaunch kelsey_topics fancy_topic_publisher.launc fancy_topic_subscriber.launch`.


## Getting started


Thanks to the launch files on each subpackage, it is straightfoward to get started. Following the instructions in the [Installation and Configuration](#installation-and-configuration) section will launch the desired subpackage. 

Launching the kelsey_actions package will activate the server and client nodes. You will see the time elapsed counter and the time remaining counter report about every second until 5 updates are sent.

Launching the kelsey_services package will activate the server and client nodes. You will also need to include a message (as described in the [Installation and Configuration](#installation-and-configuration)) for the counter to evaluate the number of words in the message. The output should be the number of words in the message you typed in. 

Launching the kelsey_topics package will print out real and imaginary numbers that are randomly generated, and rinted to the concole at 2 Hz.
## Usage

Additional dependencies can be added by editing `package.xml`. If you would like to add additional node files, be sure to make them user-executable by using the command `chmod u+x` in the terminal window after creating the file, and edit the launch file for that subpackage appropriately. This package is derived from the book Programming Robots with ROS: A Practical Introduction to the Robot Operating System by Morgan Quigley, Brian Gerkey, and William Smart (O’Reilly Media, 2015). Information on how to create these packages yourself can be found at http://ricopic.one/courses/robotics_mini_course/ in both print and YouTube videos by Dr. Rico Picone. A great resource for additional information on getting started with ROS can be found at https://risc.readthedocs.io/1-ros-basics.html.

## Questions
For further questions, please contact the maintainer and sole contributer of this package, Kelsey Buckles at kelsey.buckles@stmartin.edu.


