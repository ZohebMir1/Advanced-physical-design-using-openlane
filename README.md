# ADVANCED_PHYSICAL_DESIGN_OPENLANE.
` 

# Day1:  Inception of open-source EDA, OpenLANE and Sky130 PDK

## What’s Inside an IC ?

![2](https://user-images.githubusercontent.com/110513499/182810848-3ec9e0d3-1b4a-4417-8857-8428fafb5ea8.png)
  IC mainly consists of three sections:- 
  
  1) I/O ring:- The outermost section of an IC is an I/O ring, which contains pins to connect        the chip to outside electronics. It contains pins to give input as well as pins to output.
  2) DIE:- It is the size of a semiconductor or chip. It connects the I/O ring to the                semiconductor.
  3) CORE:- In the core, all the components responsible for functionality and logic are placed        such as cells, gates, etc.


## Asic physical design flow

The diagram below shows the detailed flow of physical design:
![1](https://user-images.githubusercontent.com/110513499/182806076-190e8989-3ede-4777-901b-68aa4cb3ae5a.png)
  	-source:- Mohamed Shalan, et al. 2020 IEEE/ACM International Conference On Computer Aided Design (ICCAD)

  Synthesis:- In synthesis, an RTL code designed by frontend is converted into gate level         circuit and is stored in the form of a gate level netlist. Open source softwares:-
   1) Yosys:- It is used to do the synthesis and generates gate level netlist. 
   2) ABC:- It is used to map the gate level netlist with the models of gates available in the         standard cells library.
   3) OpenSTA:- It is used to perform static timing analysis and check for any timing violations       before even actually placing all the cells.

  DFT:- It stands for Design for testability. In order to test a small batch of IC’s after         getting manufactured and before getting shipped, DFT is used. The tool adds certain circuitry   in order to test for any manufacturing defects for the design components inside the IC using     Automatic test pattern generator (ATPG). Open source softwares:-
   1)Fault:- It is used to implement DFT in the design.
 
  Floorplanning, Placements and Routing, CTS and Optimization:- After the synthesis and STA is     done, the actual placements of components from the gate level netlist needs to be done.         Initially floorplanning is done which is deciding the cross-sectional area of the chip. After   floorplanning, placement is done in which components are placed into the planned floorplan.     Then, connections need to be made between these components as indicated in gate level netlist.   This is done at the routing stage. Further, the circuit is optimized. Softwares:- 
   1) openROAD app

  Logic Equivalence Checking (LEC):- After the floorplanning, placements, routing and             optimization, the circuit design will be modified. Hence, to make sure the new circuit design   maintains the same functionality, LEC check is done. Open source software:-
   1) Yosys.

  Physical Verification:- After the layout is designed, physical verification of the layout       needs to be done. In physical verification, various checks are done such as Design Rule check   (DRC), Layout vs Schematic (LVS). In DRC, the tool checks for various design rules such as       minimum metal spacing, overlapping of metals, via spacing,etc. In LVS, the tool checks           whether the layout is functioning the same as schematic by generating a netlist of the layout   design and also using the netlist obtained after synthesis then these netlists are run to       check whether the outputs are same for both. Open source softwares used:-
   1) Magic:- It is used for checking DRC errors.
   2) Magic and Netgen:- These both tools are used in combination to check for LVS violations.

## Components needed for ASIC

![3](https://user-images.githubusercontent.com/110513499/182813485-c0ceaa23-523e-459d-9b54-35538c8d9930.png)

  Inputs of ASIC (Physical Design):- 
   1) RTL designs:- For physical design of an IC to be done, there is a need for the frontend        design of that particular IC, which is called as RTL design. For open source RTL designs        the sources are as follows:-
     a) Librecores.org
     b) Opencores.org
     c) Github.com

   2) EDA tools:- To make a physical design, which is the layout of an IC, EDA tools are needed      in almost each and every step of the process such as timing analysis, floorplan, placement      and routing, verification. The open source EDA tools are as follows:-
     a) OpenLane
     b) Qflow
     c) OpenRoad

  3) PDK(Process design kits):- In the current scenario, not every IC design company is also         manufacturing the IC. For manufacturing of the IC, there are special fabrication units. In       order to design an IC to be fabricated by some other units there is a need for communication     to get process details for IC to be manufactured, this communications are done by various       files which are provided by the fabs. PDK’s contain all such files and they are specific to     the technology such as 130 nm. The open source PDK’s are as follows:-
    a) Skywater-pdk 130 nm.

  Outputs of ASIC design:-
  1) Layout (GDS11):- It is generated at the end of the design flow. It is a database format          which contains complete design with layout.

## StriVe and its features

StriVe is an SOC family designed by efabless with everything open source such as EDA tools, PDK’s and RTL designs. Below image shows the complete family of StriVe with its features.
![4](https://user-images.githubusercontent.com/110513499/182821233-517e9573-956a-428e-84a3-8427b83d6512.png)

## PDK File Directory
![5](https://user-images.githubusercontent.com/110513499/182821763-ec222f45-c795-4a1a-98db-875d8bde238f.png)

There are 3 pdk files in the directory
 1) Skywater-pdk :-  This file contains each and every file related to the process design           kit(PDK) of Skywater 130 nm such as timing libraries, LEF (library exchange format).

 2) Open_pdk:- The Skywater-pdk contains files related to the process but they are generated for     the commercial EDA tools. As we are using an open source EDA tool, there is a need to           convert this file into a file which is compatible with the open source EDA tool. Open_pdk       contains the scripts and files which are used to convert files which are non compatible open     source to the files which are compatible with them.

 3) sky130A:- This is the particular pdk file which is made compatible with open source tools.       This file contains reference libraries with respect to technology and process variations.

## Opening the openLane tool
![6](https://user-images.githubusercontent.com/110513499/182824775-26e965f3-5f13-4480-9eb4-f2f9bc6d5ab9.png)

The script is run which is known as flow.tcl, this script starts the openLane tool. It also uses argument in order to use openLane in either of the two modes available which are interactive and autonomous mode.

![7](https://user-images.githubusercontent.com/110513499/182824947-9dc8e4e6-f3c9-4668-969e-6edf875a1862.png)

## Contents of design folder
![8](https://user-images.githubusercontent.com/110513499/182825327-e961be1a-f05b-4f33-9da4-0631e58f266f.png)

It contains scripts which are used to configure pdks. It also contains a src folder which contains verilog netlist which needs to be synthesized. It also contains a design constraint file which contains logical constraints of the design. It also contains a config file which configures the design and some parameters which need to be changed from default such as clock period and file paths. The run folder contains the generated files after a successful run, it also contains results, commands executed, logs of the terminal.

## Design setup

Synthesis needs various inputs such as RTL code from the front-end and standard cell libraries which will be used to map the RTL netlist generated after synthesis with the standard cells, this is done by ABC software in our project. All these files need to be set up before running the synthesis.

This is done by using the command “prep -design $filename”, as shown below. However before even doing the design setup all the packages which will be needed in the process are imported using command “package require openlane 0.9”.

![9](https://user-images.githubusercontent.com/110513499/182826413-8b5e4ce0-9e2d-40a4-a4ec-687a8cc98957.png)

![10](https://user-images.githubusercontent.com/110513499/182826566-ac113bee-f8b1-4a80-b3a2-80046abebe7e.png)

## Synthesis

Synthesis:- To perform synthesis run command: run_synthesis
![11](https://user-images.githubusercontent.com/110513499/182827849-29f514be-2852-4df1-9c09-046392abb5bc.png)

To calculate ratio of D flip flop to total number of cells:-
![12](https://user-images.githubusercontent.com/110513499/182828109-17962dd2-1170-4e51-adb9-6d53597f71a3.png)

Ratio= 1613/14786 =0.1090 or 10.9%







