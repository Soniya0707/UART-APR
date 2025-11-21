## AIM:

To implement and design synthesis and simulation for uart using cadence - genus and innovus.

## TOOLS REQUIRED:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim) Synthesis: Genus Floorplanning: Innovus

## PROCEDURE:

Step 1: Synthesis requires the following files as follows: ◦ Liberty Files (.lib) ◦ VerilogFiles (.v )

### Add Verilog  (.v ) file

### Add Testbench file

### Add run.tcl file

SDC (Synopsis Design Constraint) File (.sdc)

In your terminal type “gedit input_constraints.sdc” to create an SDC File if you do not have one.

The SDC File must contain the following commands; 

### Add SDC file

i→ Creates a Clock named “clk” with Time Period 2ns and On Time from t=0 to t=1. 

ii, iii → Sets Clock Rise and Fall time to 100ps. 

iv → Sets Clock Uncertainty to 10ps. 

v, vi → Sets the maximum limit for I/O port delay to 1ps.

•	The Liberty files are present in the library path,

•	The Available technology nodes are 180nm ,90nm and 45nm.

•	In the terminal, initialise the tools with the following commands if a new terminal is being used. ◦ csh ◦ source /cadence/install/cshrc

•	The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

•	Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist. Step 2 : Creating an SDC File Step 3 : Performing Synthesis

### Fig 1: RTL Simulation:
![WhatsApp Image 2025-11-21 at 21 46 02_b4936b41](https://github.com/user-attachments/assets/ee76a9cc-627f-4d5a-9ac9-798ae3516bca)


### Fig 2: Synthesis RTL Schematic:
![WhatsApp Image 2025-11-21 at 21 55 15_662a17ed](https://github.com/user-attachments/assets/ab142ee3-40f1-44f4-8c28-fb4fea89a87d)


### Fig 3: Area Report:
<img width="1920" height="1080" alt="Screenshot (392)" src="https://github.com/user-attachments/assets/78d1dbf6-3119-4318-bf84-d08a1fe1d666" />


### Fig 4: Power Report:
<img width="1920" height="1080" alt="Screenshot (390)" src="https://github.com/user-attachments/assets/971806cc-d630-46dd-8829-51b84b8c3091" />


### Fig 5: Timing Report:
<img width="1920" height="1080" alt="Screenshot (391)" src="https://github.com/user-attachments/assets/4bfc1875-eb22-45ae-bbfa-f69c8a1b6800" />


### Fig 6: UART APR:

## RESULT:

The functionality of the uart was successfully verified using a testbench and simulated with the nclaunch tool and genus and for innovus creating the physical design.
