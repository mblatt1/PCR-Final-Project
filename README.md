# PCR-Final-Project
Group Members: Martha Blatt and Mary Lynn Dekold

This is a repository with the Jupyter notebooks that comprise the final project for CBE 30338.

Purpose: The purpose of the final project was to design a control system for a PCR thermal cycler in Python and to test the control system using a Temperature Control Laboratory. 

Goal: To design a control system that maintains the heater temperature of the TCLab within 2 degrees of a control trajectory specified by the user.

Implementation: The control algorithm used was model predictive control (MPC). Using MPC, the heater was able to remain within two degrees of the specified setpoint throughout the control trajectory. The largest deviation from the setpoint occurred during the cooling of the device, a physical limitations of the device itself. 
