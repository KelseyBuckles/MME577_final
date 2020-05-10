

# ROS package: MME577_final

This package includes 3 subpackages: kelsey_topics, kelsey_actions, kelsey_services, along with their corresponding launch files.
kelsey_topics contains message and topic publisher and subscriber nodes under the names message_publisher.py, message_subscriber.py, topic_publisher.py, and topic_subscriber.py which allows nodes to communicate by publishing (speaking), and subscribing (listening).
This package also includes a custom message description--Complex.msg--for messages containing real and imaginary numbers.
kelsey_actions is where subpackages that ask nodes to actually DO things would live. Currently, the only action is Timer.action, which waits a certain amount of time, keeps track of the total actual wait time and total number of feedback updates sent, and prints time elapsed and time remaining as feedback on each time step (note that this is different from a service since it provides feedback during execution).
kelsey_services includes subpackages where one node provides a function to the other nodes. Currently the only service file in there is WordCount.srv, which counts words.

## Requirements

This system will work on Linux based machines running Ubuntu Bionic 18.04.4, ROS Melodic Morenia, and Python 2.

## Installation and configuration

|Instructions for installation and configuration. Assume users know how to install ROS packages and can use `git`.|
Once your machine is setup with ROS Melodic Morenia, Python 2, and git, fork and clone this repository from a terminal window in your machine, into a ROS workspace's src directory. Then, navigate to your workspace root, and source the package using 'catkin_make'

## Getting started

|A short guide to using your package. Include important commands, etc.|

## Usage

|Usage information for key methods and commands.|

## Questions
For further questions, please contact the maintainer and sole contributer of this package, Kelsey Buckles at kelsey.buckles@stmartin.edu.


