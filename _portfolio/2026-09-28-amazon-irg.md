---
title: "Amazon Industrial Robotics Group"
seo_title: "Amazon Industrial Robotics Internship | Kushal Agarwal"
excerpt: "Working on development of highly dynamic industrial robot capable of performing human like tasks across locomotion and manipulation"
collection: portfolio
---

PS: This page is intentionally vague

## Overview
Industrial Robotics Group at Amazon is building revolutionary robotic systems that combine innovative AI, sophisticated control systems, and advanced mechanical design to create adaptable automation solutions capable of working safely alongside humans in dynamic environments. The team is developing advanced robots along the axis of robotic manipulation, locomotion, and human-robot interaction. 

I had the opportunity to work with [Yuri Ivanov](https://www.amazon.science/author/yuri-ivanov)'s RnD team to develop robotic and perception systems with rigorous scientific analysis to guide product development.  

## My contributions

### State estimation and control in dynamic robot systems with closed chains

Robots that have discontinuous ground contact have unique dynamics with each contact state. For fast localization of the pose of a root link of the robot, such dynamics have to be used with proprioceptive robot state measurement. Such dynamic systems also require high frequency and precise control especially when the kinematic structure contains closed chains. 

I integrated an invariant-EKF with robot dynamics served by pinocchio and proprioceptive data from joint encoders, IMU, and contact pressure sensors. This could provide accurate 6 DoF pose estimation of the root link. I also explored various contact models to map contact pressure readings and data from other sensors to model contact state transitions. 

For controlling closed loop chains with 4 joints (2 input and 2 output), I developed an output space impedance controlled with a control barrier function to get safe and simplified output joint dynamics. 

### Precise and simultaneous calibration of exteroceptive sensor

Given a rigid arrangement of RGB cameras, thermal(LWIR) cameras and LiDARs, I developed algorithms and procedures for intrinsic and extrinsic calibration at manufacturing-scale and precision.

RGB and LWIR sensors measure a large span of wavelengths and developing calibration target that could provide identifiable, diverse, and distinguishable points across multiple wavelengths is non-trivial. Having simultaneous targets allows single shot calibration of both sensors saving time, space and money as an alternate to having separate procedures per sensor and then an extrinsic calibration. To this end, I developed custom calibration targets that could be visible in the full visible to far IR spectrum. 

Positioning the sensors with respect to calibration boards defined the diversity of data for calibration. Having poor data diversity can severely lower the observability of various camera model and extrinsic parameters. It is important to carefully choose these positions to maximize the amount of sensitivity that a dataset can provide with respect to the parameters. For optimally choosing these viewpoints, I used Fischer information to evaluate a set of viewpoints for excitation of camera model parameters and maximized the information (determinant) with respect to the trajectory for optimal positioning. 

<figure>
  <img src="/images/portfolio/amazon/trajectory_opti.gif">
  <figcaption>The solver is initialized with a simple circular trajectory, as shown on the left. The resultant optimized trajectory is on the right. The sensor system consists of 4 cameras (C1-4) placed in a radially outward looking orientation on a circle.</figcaption>
</figure>
I assembled a full calibration system, with a robot to move this rigid group of sensors with respect to the calibration boards with the optimal poses chosen. This data is collected and then an optimizer calculated the camera model parameters. The result is validated for reaching the global minimum and correspondingly the result is accepted. 



