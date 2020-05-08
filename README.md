# PCR Final Project
This is a repository with the Jupyter notebooks that comprise the final project for CBE 30338.

**Group Members**: Martha Blatt and Mary Lynn Dekold

**Purpose**: To design a control system for a PCR thermal cycler in Python and to test the control system using a Temperature Control Laboratory. 

**Goal**: To create a control system that maintains the heater temperature of the TCLab within 2 degrees of a control trajectory specified by the user.

**Implementation**: The control algorithm used was model predictive control (MPC). Using MPC, the heater was able to remain within two degrees of the specified setpoint throughout the control trajectory. The largest deviation from the setpoint occurred during the cooling of the device, which is result of the physical limitations of the device itself. 

## Jupyter Notebooks

**Protocol UI**: [Protocol Notebook](https://github.com/mblatt1/PCR-Final-Project/blob/master/Protocol%20UI.ipynb) This notebook allows the user to specify the number of PCR thermal cycles and the time and temperature of the denaturation, annealing, and extension segments of the cycle. The protocols chosen by the user are saved in a csv file for later use. 

**Runtime UI**: [insert notebook link] This notebook allows the user to select a saved protocol for each of the two heaters. The user may view the selected protocols and with a click of the start button, the PCR cycles begin. MPC control adjusts the power input to the heaters in order to keep the heater temperature within 2 degrees of the setpoint. The run continues until either the run completes or the user presses a stop button. After the run is terminated, a record of the run is saved to a csv file and the total time required to complete the run is printed. 

**Review UI**: [Review Notebook](https://github.com/mblatt1/PCR-Final-Project/blob/master/Review%20UI.ipynb) This notebook allows the user to visualize past runs of the PCR thermal cycler. A dropdown menu displays the available files to the user. The user may select a file and then a plot is created with subplots. In the first subplot is the temperature of heater one (T1) and setpoint 1 (SP1). The second subplot has the temperature of heater 2 (T2) and setpoint 2 (SP2). The third subplot plots the power input to heater one (U1) and heater two (U2). Finally, the fourth subplot plots the deviation from the setpoint for both heater 1 and heater 2. 
