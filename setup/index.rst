Setup
=====

This section guides you through the setup process for your robot development environment.

Installing Required Software
----------------------------

1. **Ubuntu**: Install the latest version of Ubuntu.
2. **ROS**: Follow the instructions to install ROS (Robot Operating System).
3. **Development Tools**: Install necessary development tools like Python, C++, and VSCode.

.. code-block:: bash

   sudo apt update
   sudo apt install python3 python3-pip git
   sudo apt install ros-noetic-desktop-full

Configuring the Environment
---------------------------

- Set up the ROS environment by sourcing the ROS setup script.
- Configure your development environment (IDE, version control, etc.).

.. code-block:: bash

   echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc

