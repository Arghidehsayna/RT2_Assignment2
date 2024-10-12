

# Research Track Project

This repository contains the source code and related files for a robotics project developed as part of the **Research Track**. It is built using **ROS (Robot Operating System)** and includes various components such as robot simulation, nodes, actions, and configuration files.

## Table of Contents

- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Running the Project](#running-the-project)
- [License](#license)

## Project Structure

- **action/**: Contains ROS actions that define tasks executed by the nodes.
- **build/**: The build directory, typically generated after compiling the code.
- **config/**: Configuration files for various aspects of the system.
- **docs/**: Documentation for the project. You can generate it using Doxygen and the provided `Doxyfile`.
- **launch/**: ROS launch files that start up various nodes and the simulation.
- **msg/**: Custom ROS message definitions used by the project.
- **scripts/**: Python scripts, possibly defining ROS nodes or utilities.
- **source/**: Core source code of the project.
- **urdf/**: Contains robot models in URDF format for simulation purposes.
- **world/**: Simulation environment setup files (possibly for Gazebo).
- **NodeA.ipynb**: Jupyter notebook related to a specific node in the system.
- **package.xml**: ROS package manifest listing dependencies and project metadata.
- **CMakeLists.txt**: CMake configuration file used for building the project.
- **Makefile**: Makefile to build the project in Linux environments.
- **Doxyfile**: Doxygen configuration file for generating project documentation.

## Dependencies

To run this project, you'll need the following dependencies:

- **ROS Noetic** or later
- **Gazebo** (for robot simulation)
- **Python 3.x**
- **CMake** (for building the project)
- **Doxygen** (for generating documentation)

Make sure all the necessary ROS packages are installed. Refer to the `package.xml` for the list of dependencies.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/research-track.git
   cd research-track
   ```

2. Install the required ROS packages:
   ```bash
   rosdep install --from-paths src --ignore-src -r -y
   ```

3. Build the project:
   ```bash
   catkin_make
   ```

4. Source the workspace:
   ```bash
   source devel/setup.bash
   ```

## Running the Project

You can run the project using the provided launch files. For example:

```bash
roslaunch research_track <launch_file_name>.launch
```

Ensure you have a running ROS master node before launching.

## Documentation

You can generate the documentation using Doxygen. To do so:

```bash
doxygen Doxyfile
```

This will generate the HTML documentation in the `docs/` directory.
