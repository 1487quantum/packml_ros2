# packml_ros2 Documentation

This package implements a state machine as prescribed in the Packaging Machine Language (PackML) standard in simulation. 

This package also contains an RViz 2 plugin to be able to visualize the state of the state machine, the elapsed time in that state, and to control the triggering of state transitions of the machine through buttons. 

Finally, the package contains an example of the interface of the RViz2 plugin with a real PackML state machine running in a PLC, communicating its state and triggering transitions via OPCUA public tags. 

## List of packages
* `packml_plugin`: RViz2 plugin for PackML state machine standard template visualization and control
* `packml_sm`: Simulator library in C++ ported to ROS 2 from the original PackML repository in ROS 1. Two types of state machines, with continuous Execute state and with timed Execute state.
* `packml_msgs`: Service type definitions for states, transitions and GUI control
* `packml_ros`: ROS 2 node in C++ to run the simulator library and communicate with the RViz2 plugin.

Extras:
* `packml_plc`: Example of a driver in Python to interface with a PackML state machine implemented in a Siemens PLC (with pre-configured OPCUA variable tags according to the PLCs configuration). Direct communication with the RViz2 plugin (receive states and send events to trigger transitions). 
