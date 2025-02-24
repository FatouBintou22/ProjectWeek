---
layout: pw39-project

permalink: /:path/

project_title: SlicerROS2
category: IGT and Training
presenter_location: In-person

key_investigators:

- name: Junichi Tokuda
  affiliation: Brigham and Women's Hospital
  country: USA

- name: Laura Connolly
  affiliation: Queen's University
  country: Canada

- name: Anton Deguet
  affiliation: Johns Hopkins University
  country: USA

- name: Arvind S. Kumar,
  affiliation: Johns Hopkins University
  country: USA

---

# Project Description

<!-- Add a short paragraph describing the project. -->

The goal of SlicerROS2 is to provide an open-source software platform for medical robotics research. Specifically, the project focuses on architectures to seamlessly integrate a robot system with medical image computing software using two popular open-source software packages: Robot Operating System (ROS) and 3D Slicer.

## Objective

<!-- Describe here WHAT you would like to achieve (what you will have as end result). -->

1.  Demo - Set up a live demo using SlicerROS2 and [myCobot](https://www.elephantrobotics.com/en/mycobot-en/).
2.  Dissemination - Review and improve online documentation for rosmed.github.io
3.  Plan - Discuss future directions and maintenance (other potential projects, integration into nightly build, etc).

## Approach and Plan

<!-- Describe here HOW you would like to achieve the objectives stated above. -->

1.  Set up a build environment on a laptop with Ubuntu 22.04
2.  Set up myCobot

## Progress and Next Steps

<!-- Update this section as you make progress, describing of what you have ACTUALLY DONE.
     If there are specific steps that you could not complete then you can describe them here, too. -->

1.  Set up ROS2 Humble Hawksbill on Ubuntu 22.04 [ROS2 Humble Installation on Ubuntu (Debian)](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)
2.  Built the SlicerROS2 estension [Slicer ROS2 Getting Started](https://slicer-ros2.readthedocs.io/en/latest/pages/getting-started.html)
  - The Slicer ROS2 could not be compiled due to an issue in the CMakeLists.txt. It has been fixed and incorporated into the main repository ([pull request on GitHub](https://github.com/rosmed/slicer_ros2_module/pull/66) )
4.  Set up ROS interface for myCobot [Github repository]( https://github.com/elephantrobo,cs/mycobot_ros2 )
  - Change the name of the device file in line 14 in listen_real.py ('/dev/5yUSB0') to '/dev/5yACM0'.
5.  Replace the robot model in the ros interface.
6.  Launch the interface by:
~~~~
ros2 launch mycobot_280 slider_control.launch.py
~~~~

# Illustrations

<!-- Add pictures and links to videos that demonstrate what has been accomplished. -->
 <iframe width="420" height="315" src="https://www.dropbox.com/s/tbg77pgedba6lys/SlicerROS2_myCobot_Montreal_June2023.mov?dl=0">
 </iframe>

# Background and References

<!-- If you developed any software, include link to the source code repository.
     If possible, also add links to sample data, and to any relevant publications. -->

The National Institute of Biomedical Imaging and Bio-engineering of the U.S. National Institutes of Health (NIH) under award number R01EB020667, and 3R01EB020667-05S1 (MPI: Tokuda, Krieger, Leonard, and Fuge). The content is solely the responsibility of the authors and does not necessarily represent the official views of the NIH.

The National Sciences and Engineering Research Council of Canada and the Canadian Institutes of Health Research, the Walter C. Sumner Memorial Award, the Mitacs Globalink Award and the Michael Smith Foreign Study Supplement.
