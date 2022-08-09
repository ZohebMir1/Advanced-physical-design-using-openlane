# Table of content
- Day1
  - [What’s Inside an IC](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#whats-inside-an-ic-)  
  - [Asic physical design flow](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#asic-physical-design-flow)
  - [Components needed for ASIC](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#components-needed-for-asic)
  - [StriVe and its features](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#StriVe-and-its-features)
  - [PDK File Directory](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#pdk-file-directory)
  - [Opening the openLane tool](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#opening-the-openLane-tool)
  - [Contents of design folder](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#contents-of-design-folder)
  - [Design setup](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#design-setup)
  - [Synthesis](https://github.com/ZohebMir1/VSD_WKSHP/edit/main/README.md#synthesis)
 
- Day2
  - [List of all switches/functions available for using this software](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#list-of-all-switchesfunctions-available-for-using-this-software)
  - [Default conifguration of tool for floorplan](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#Default-conifguration-of-tool-for-floorplan)
  - [Configuration file](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#configuration-file)
  - [Sky130 file](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#Sky130-file)
  - [Precedence of configuration, default file, sky130](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#Precedence-of-configuration-default-file-sky130)
  - [How to run floorplan](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-run-floorplan)
  - [Output file after the floorplan](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#output-file-for-the-floorplan)
  - [Magic sofware and how to use it in openlane flow](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#magic-sofware-and-how-to-use-it-in-openlane-flow-)
  - [How to use magic for floorplan](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-use-magic-for-floorplan)
  - [Change on the go in the interactive mode](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#change-on-the-go-in-the-interactive-mode)
  - [Example of a functions of floorplan in openlane](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#example-of-a-functions-of-floorplan-in-openlane)

- Day3
  - [Steps to open a cell in magic](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#steps-to-open-a-cell-in-magic)
  - [Steps to extract spice file from the layout](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#steps-to-extract-spice-file-from-the-layout)
  - [How to run the analysis in ngspice](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-run-the-analysis-in-ngspice)
 
 - Day4
   - [Pre LEF generation tasks for a standard cell](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#pre-lef-generation-tasks-for-a-standard-cell)
   - [How to extract a lef file from magic](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-extract-a-lef-file-from-magic)
   - [How to insert our designed cell into the pre-designed block](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-insert-our-designed-cell-into-the-pre-designed-block)
   - [Steps to invoke sta tool](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#steps-to-invoke-sta-tool)\
   - [how to improve timing violations in a pre layout sta](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-improve-timing-violations-in-a-pre-layout-sta)
   - [Manually reduce slack](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#manually-reduce-slack)
   - [How to run cts](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#how-to-run-cts)

 - Day5
   - [Generation of power distribution network PDN](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#generation-of-power-distribution-network-pdn)
   - [Output of pdn](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#output-of-pdn)
   - [Running routing](https://github.com/ZohebMir1/Advanced-physical-design-using-openlane/edit/main/README.md#running-routing)

# ADVANCED_PHYSICAL_DESIGN_OPENLANE.

## Day1:  Inception of open-source EDA, OpenLANE and Sky130 PDK

### What’s Inside an IC ?

 ![2](https://user-images.githubusercontent.com/110513499/182810848-3ec9e0d3-1b4a-4417-8857-8428fafb5ea8.png)
  IC mainly consists of three sections:- 
  
  1) I/O ring:- The outermost section of an IC is an I/O ring, which contains pins to connect the chip to outside electronics. It contains pins to give input as well as pins to output.
  2) DIE:- It is the size of a semiconductor or chip. It connects the I/O ring to the semiconductor.
  3) CORE:- In the core, all the components responsible for functionality and logic are placed such as cells, gates, etc.


### Asic physical design flow

The diagram below shows the detailed flow of physical design:
![1](https://user-images.githubusercontent.com/110513499/182806076-190e8989-3ede-4777-901b-68aa4cb3ae5a.png)
  	-source:- Mohamed Shalan, et al. 2020 IEEE/ACM International Conference On Computer Aided Design (ICCAD)

  Synthesis:- In synthesis, an RTL code designed by frontend is converted into gate level circuit and is stored in the form of a gate level netlist. Open source softwares:-
   1) Yosys:- It is used to do the synthesis and generates gate level netlist. 
   2) ABC:- It is used to map the gate level netlist with the models of gates available in the standard cells library.
   3) OpenSTA:- It is used to perform static timing analysis and check for any timing violations before even actually placing all the cells.

  DFT:- It stands for Design for testability. In order to test a small batch of IC’s after getting manufactured and before getting shipped, DFT is used. The tool adds certain circuitry   in order to test for any manufacturing defects for the design components inside the IC using Automatic test pattern generator (ATPG). Open source softwares:-
   1)Fault:- It is used to implement DFT in the design.
 
  Floorplanning, Placements and Routing, CTS and Optimization:- After the synthesis and STA is done, the actual placements of components from the gate level netlist needs to be done. Initially floorplanning is done which is deciding the cross-sectional area of the chip. After   floorplanning, placement is done in which components are placed into the planned floorplan. Then, connections need to be made between these components as indicated in gate level netlist.   This is done at the routing stage. Further, the circuit is optimized. Softwares:- 
   1) openROAD app

  Logic Equivalence Checking (LEC):- After the floorplanning, placements, routing and optimization, the circuit design will be modified. Hence, to make sure the new circuit design maintains the same functionality, LEC check is done. Open source software:-
   1) Yosys.

  Physical Verification:- After the layout is designed, physical verification of the layout needs to be done. In physical verification, various checks are done such as Design Rule check   (DRC), Layout vs Schematic (LVS). In DRC, the tool checks for various design rules such as minimum metal spacing, overlapping of metals, via spacing,etc. In LVS, the tool checks whether the layout is functioning the same as schematic by generating a netlist of the layout   design and also using the netlist obtained after synthesis then these netlists are run to check whether the outputs are same for both. Open source softwares used:-
   1) Magic:- It is used for checking DRC errors.
   2) Magic and Netgen:- These both tools are used in combination to check for LVS violations.

### Components needed for ASIC

![3](https://user-images.githubusercontent.com/110513499/182813485-c0ceaa23-523e-459d-9b54-35538c8d9930.png)

  Inputs of ASIC (Physical Design):- 
   1) RTL designs:- For physical design of an IC to be done, there is a need for the frontend design of that particular IC, which is called as RTL design. For open source RTL designs the sources are as follows:-
     a) Librecores.org
     b) Opencores.org
     c) Github.com

   2) EDA tools:- To make a physical design, which is the layout of an IC, EDA tools are needed in almost each and every step of the process such as timing analysis, floorplan, placement and routing, verification. The open source EDA tools are as follows:-
     a) OpenLane
     b) Qflow
     c) OpenRoad

  3) PDK(Process design kits):- In the current scenario, not every IC design company is also manufacturing the IC. For manufacturing of the IC, there are special fabrication units. In order to design an IC to be fabricated by some other units there is a need for communication to get process details for IC to be manufactured, this communications are done by various files which are provided by the fabs. PDK’s contain all such files and they are specific to     the technology such as 130 nm. The open source PDK’s are as follows:-
    a) Skywater-pdk 130 nm.

  Outputs of ASIC design:-
  1) Layout (GDS11):- It is generated at the end of the design flow. It is a database format which contains complete design with layout.

### StriVe and its features

StriVe is an SOC family designed by efabless with everything open source such as EDA tools, PDK’s and RTL designs. Below image shows the complete family of StriVe with its features.
![4](https://user-images.githubusercontent.com/110513499/182821233-517e9573-956a-428e-84a3-8427b83d6512.png)

### PDK File Directory
![5](https://user-images.githubusercontent.com/110513499/182821763-ec222f45-c795-4a1a-98db-875d8bde238f.png)

There are 3 pdk files in the directory
 1) Skywater-pdk :-  This file contains each and every file related to the process design kit(PDK) of Skywater 130 nm such as timing libraries, LEF (library exchange format).

 2) Open_pdk:- The Skywater-pdk contains files related to the process but they are generated for the commercial EDA tools. As we are using an open source EDA tool, there is a need to convert this file into a file which is compatible with the open source EDA tool. Open_pdk contains the scripts and files which are used to convert files which are non compatible open source to the files which are compatible with them.

 3) sky130A:- This is the particular pdk file which is made compatible with open source tools. This file contains reference libraries with respect to technology and process variations.

### Opening the openLane tool
![6](https://user-images.githubusercontent.com/110513499/182824775-26e965f3-5f13-4480-9eb4-f2f9bc6d5ab9.png)

The script is run which is known as flow.tcl, this script starts the openLane tool. It also uses argument in order to use openLane in either of the two modes available which are interactive and autonomous mode.

![7](https://user-images.githubusercontent.com/110513499/182824947-9dc8e4e6-f3c9-4668-969e-6edf875a1862.png)

### Contents of design folder
![8](https://user-images.githubusercontent.com/110513499/182825327-e961be1a-f05b-4f33-9da4-0631e58f266f.png)

It contains scripts which are used to configure pdks. It also contains a src folder which contains verilog netlist which needs to be synthesized. It also contains a design constraint file which contains logical constraints of the design. It also contains a config file which configures the design and some parameters which need to be changed from default such as clock period and file paths. The run folder contains the generated files after a successful run, it also contains results, commands executed, logs of the terminal.

### Design setup

Synthesis needs various inputs such as RTL code from the front-end and standard cell libraries which will be used to map the RTL netlist generated after synthesis with the standard cells, this is done by ABC software in our project. All these files need to be set up before running the synthesis.

This is done by using the command “prep -design $filename”, as shown below. However before even doing the design setup all the packages which will be needed in the process are imported using command “package require openlane 0.9”.

![9](https://user-images.githubusercontent.com/110513499/182826413-8b5e4ce0-9e2d-40a4-a4ec-687a8cc98957.png)

![10](https://user-images.githubusercontent.com/110513499/182826566-ac113bee-f8b1-4a80-b3a2-80046abebe7e.png)

### Synthesis

Synthesis:- To perform synthesis run command: run_synthesis
![11](https://user-images.githubusercontent.com/110513499/182827849-29f514be-2852-4df1-9c09-046392abb5bc.png)

To calculate ratio of D flip flop to total number of cells:-
![12](https://user-images.githubusercontent.com/110513499/182828109-17962dd2-1170-4e51-adb9-6d53597f71a3.png)

Ratio= 1613/14786 =0.1090 or 10.9%

## Day2:- Good floorplan VS Bad floorplan and introduction to library cells

### List of all switches/functions available for using this software
In current scenario, as the work is automated and done by the software. Its important to instruct the tool what you expect the tool to do. All the functions which can be used in openLane tool to command it are listed in the below images.
![1](https://user-images.githubusercontent.com/110513499/183488587-a0be2640-8f75-480a-a7e8-7d4f22635e7e.png)
![2](https://user-images.githubusercontent.com/110513499/183491475-1f354fa1-8bd6-460e-ac3c-9565f10c0b09.png)

### Default conifguration of tool for floorplan
If we did not instruct the software by not using any of the above shown commands, how will the tool work ? So, the tool already has a few default commands set. If we did not write a few commands tool does the work as instructed by default functions in one of the configuration files. The images below indicates the default functions for openLane software.
![3_floorplan tcl](https://user-images.githubusercontent.com/110513499/183492624-d4ecf61a-a3a0-425e-a8c6-09b1f5c48844.png)
![4-floorplan tcl](https://user-images.githubusercontent.com/110513499/183492646-75066c58-dbed-43ae-ac86-455e7d3d44e6.png)

### Configuration file
The configuration file is present inside the openLane directory. The software also reads this file in order to understand the functions it has to do. The image below shows the configuration file and the functions instructed to the tools by this file.
![6_config,tck](https://user-images.githubusercontent.com/110513499/183495165-47a429a5-8aae-4ab0-bcfd-1025baa02f3c.png)

### Sky130 file
It is also similar to the above two files which helps the users to command the tool. The image of this file has been shown below.
![7_sky130](https://user-images.githubusercontent.com/110513499/183495938-9524740f-16dc-466a-916d-2a5711ff8393.png)

### Precedence of configuration, default file, sky130
You may wonder, if I give a same function in all the files but with different way of doing the same thing. What will the tool do ? So, the tool gives priority or higher power to some files which means that if a same function is set in all the files it will accept the value only from the file which has highest precedence. If a function is given in only two files, it will accept that variable from the file with highest precedence of both. Precedence of the tools are listed below.

Sky130 file > configuration file > foorplan file.
So, sky130 file has the highest priority and floorplan.tcl will have the least probability


### How to run floorplan 
In the updated version of openLane software, the set of commands to execute various tasks without any error in openLane has been changed from the previous one. So, in order to run floorplan. We use the command below:-

init_floorplan

### Output file for the floorplan
The floorplan generates a file in the def format. DEF stands for data exchange format. This file contains the physical view of the project with every physical detail such as dimensions, contents in each row of a die(semiconductor),etc. The def file which was generated after floorplan will contain dimensions and location of the die, io ports, tap cells with also their detailed physical view.

### Magic sofware and how to use it in openLane flow:-
If we recall from the flow chart of openLane, we will get to know about the various softwares used in the openLane flow. One of the softwares used in this flow is Magic. If we want to physically see our project, we will have to use Magic software. To open Magic software, we will have to use the below command:-
Magic -T <tech file path> lef read <lef file path> def read <def file path>.

The below image shows an example command which was used to open floorplan
![8](https://user-images.githubusercontent.com/110513499/183498480-62dded01-fa9d-40ac-b1e3-9679075d2a95.png)

The image below shoes the view of the file when it is openend using Magic software. 
![9_layout_magic](https://user-images.githubusercontent.com/110513499/183500748-2c7fe459-1c23-467f-aa82-e0feec1a58aa.png)

### How to use magic for floorplan
 - How to select a block in Magic ?
    To open a blow in magic scroll over that block and press s. It will select the block
 
 - How to view which details of the cell(block) ?
    To view the details of the block such as its name, it is made of which metal layers. Give the command "what" after selecting that block in the tkcon window. Tkcon     window is basically a window created when we run Magic, to give any commands to the Magic software we give it in this window. The image below shows one of the         examples of the command "what".
    ![10_what](https://user-images.githubusercontent.com/110513499/183502367-5fbc2e7b-f33d-45c7-ba6b-c478f4672f31.png)

### Change on the go in the interactive mode
The openLane tool in its interactive mode allows to change the functions on the go in between various stages of the VLSI flow. Example of a function it shown in the below below topic.

### Example of a functions of floorplan in openLane
The function is FP_IO_MODE. This abrevation stands for floorplan_Input/output_modes. This command will set the formation of input/output modes present in the design, by formation it means spacing between all the cells of design whether it should be random or evenly spaced. If FP_IO_MODE is set to 1, the tool places all the input/output in the random manner but they are spread across the overall boundary of the design and if FP_IO_MODE is set to 0, then the tool places all the input/output in the equally distant manner but crowdedly at some instances and empty at the other.


The image below shows the command to place pins at equal distance:
![12_statement](https://user-images.githubusercontent.com/110513499/183574482-0387e102-e45e-4d94-976d-e70513d3ddea.png)

The image below shows io pins placed at random distance which resulted due to above command:
![11_floorplan_random_io](https://user-images.githubusercontent.com/110513499/183504875-9bfa2ef5-ffb5-4f41-8de9-f021e28cb7ba.png)

## Day3: Design standard cell using magic layout

### Steps to open a cell in Magic
As I explained before, Magic software provides physical view of the cell or layout. To open the standard cells file, use command Magic. The image below shows command for opening cell in the Magic layout.
![1](https://user-images.githubusercontent.com/110513499/183586906-4bdd07ec-b13a-45b1-9d02-4e8e373ddb29.png)

The image below shows the opened standard cell of inverter
![2](https://user-images.githubusercontent.com/110513499/183587158-4cca420b-3089-4fe4-ad96-5aa12b1b33b2.png)

### Steps to extract spice file from the layout
If we want to analyze a cell, to check whether its functioning as we have designed or not, we can use ngspice as a simulator for the cell. For the simulation, first step is to extract a spice file from this layout. To extract spice file run the below commands:-
 - extract all
   - This step extracts a circuit digram from the layout
  
 - ext2spice cthresh 0 rthresh 0
   - This step generates a spice file from the exracted cicuit before.
   
 The image below shoes the steps performed in Magic.
 ![4](https://user-images.githubusercontent.com/110513499/183591753-dc6364cc-ee9f-425d-8e88-0a0d8bff26f5.png)
 
 The image below shows the extracted spice file 
![3](https://user-images.githubusercontent.com/110513499/183592075-f687d077-c9bd-4c1c-a4ab-6be548e6a324.png)

If we want to run some analysis this file needs to be updated and run in ngspice. The changes needed are as follows, type of analysis you want to run, any internal parameter of the mosfets are 0, default scale needs to be changed with respect to your layout.

The image below shows the updated spice file
![6](https://user-images.githubusercontent.com/110513499/183595322-613ff22b-0351-4324-bce0-c821fbf22302.png)

### How to run the analysis in ngspice
The command used to invoke ngspice and run your design is as shown below
- ngspice "spice file name"

## Day4 Pre-Layout STA and importance of a good clock tree

### Pre LEF generation tasks for a standard cell
A standard cell always have fixed height. This is because the supply straps are placed like a grid having some distance between them. So, standard cell should always be placed in the space between vdd and vss straps which forms the grid. So, the first step is to check this.
 - Check whether the height of standard cell is the multiple of spacing between power straps:
   To check this initially we will check a file known as tracks.info which informs us about the
   metal spacing. It is a library file shown as shown below.
   ![1](https://user-images.githubusercontent.com/110513499/183607834-10ee191d-f848-4b59-a000-7d46c82f8f63.png)
   
   - Check whether tracks of the metal which is used for port intersects: Note down the particular metal layer used for forming of ports and check whether x and y direction of that metal layer intersects at the input and output ports. This helps `the tool in routing from either x or y direction both. So, it gives the tool more flexibility.
   
Method to do these checks are basically use grids of Magic software and change its width to make it same as the metal track widh then it will be clearly visible whether the heigh falls in the multiple of metal tracks and whether the metal which is used to form ports also intersect.

### How to extract a lef file from magic
 - Lef stands for library exchange format. It has an overall view of the block. It does not contain connections inside a cell. The image below shows the comparison of layout and a lef.
 ![20](https://user-images.githubusercontent.com/110513499/183599508-18254277-2fb1-490e-9980-9a354f2de2e8.png)

 - Steps to extract a lef file from Magic:- After opening Magic software, a tkcon window is always launched. This window is like a command prompt. Give the below command in this window:
    lef write 
    
    Image below shows the execution of this command
    ![4](https://user-images.githubusercontent.com/110513499/183600120-dc89df93-f6cc-4922-9c70-6e873b1e42ee.png)

The lef file generated from a standard cell of an inverter is shown below
![5](https://user-images.githubusercontent.com/110513499/183604335-c8eadfd1-1a3c-4db2-829c-4e5b9e744887.png)

### How to insert our designed cell into the pre-designed block
We already have a pre-designed netlist which went from RTL design to synthesis and the mapping of the standard cells are also done in synthesis. before synthesis, if we want our cell to be available for the tool to place it in the design, we will need to enter its lef details. As openLane provides the interactive mode, the changes can be made on the go. Steps to make these changes:-
  - Change the config.tcl and enter the paths to all the libraries such as fast corner, slow corner, typical. The image below shows the changes.
  ![9](https://user-images.githubusercontent.com/110513499/183611386-f9468caa-975d-4a57-8512-ff797ee9cdde.png)
  
  - Now run the VLSI flow until before synthesis and do changes on the go. Provide the lef file which is extracted from Magic software to the tool, so that it can also have our design to place if needed. Use the set command and create the following variable and update it. lef variable is created and lef file is added to this variable. Its implementation is shown below. 
![6](https://user-images.githubusercontent.com/110513499/183614486-2736c33b-d778-4fc4-9476-a7457f868b32.png)

  - After the synthesis, the terminal will show number of instances where our standard cell is used. Now you can continue with the flow further. The image below shows the output
  ![8](https://user-images.githubusercontent.com/110513499/183615159-da2f9235-89d3-4161-a3c7-2b92ef50b6eb.png)

### Pre layout STA

### Steps to invoke STA tool
  - Create a file of type .conf which contains all the files needed for sta and commmands to be performed in the tool. As the pre-layout sta cannot calculate the actual delays, it takes delay from library which contains delay tables. Also, it needs netlist generated after synthesis in order to check from delay table for specific cells,. Also, it needs a sdc file which contains clock details such as clock period, jitter, uncertainty, setup and hold time, etc. The below file shows an example of sta.conf file.  
![16_sta_file](https://user-images.githubusercontent.com/110513499/183617416-da72766a-2810-47c8-9248-bb5976ee2199.png)

  - To invoke tool, use command sta ".conf filemame" and run it. The below image shows the invoking steps
![15_sta_run](https://user-images.githubusercontent.com/110513499/183617752-de2b1a4f-6a0f-4f0e-82d7-6bd21dd70658.png)

### How to improve timing violations in a pre-layout STA
From the delay tables we know that delay depends on output load and input slew. So if we reduce either of these the delay will in turn reduce. Output load can be reduced by adding a buffer. We can also increase the drive strength of a cell which is having large output capacitances. The key functions of the openLane tool which can help reduce timing violations are :-
 - SYNTH_STRATEGY, if set to focus more on delay it will decrease the violation but it will also increase the area. It can be set set to 0->2. If it is 0 then tool will focus most on the delay and area can increase greatly. If set to 1 then too tool will focus more on delay and less on area but it is less strict on delay as compared to 0. If it is set to 3, then the focus will be on most on to reduce area and delay can increase. If set to 2 it will focus on area but not as strict as 3.
 
 - SYNTH_BUFFERING, if it is set to 1 then it will enable the tool to add buffers in order to reduce output load and in turn delay. If it is set to 0, then tool will be disabled.
 
 - SYNTH SIZING, if set to 1 it enables the tool to increase the drive strength of the cell which has larger fanout, in order to improve timing violations. If it is set to 0 the tool will disable this function.
 
 The image below the impact of these startegies on the delay
 Slack before using these strategies:- 
 ![13](https://user-images.githubusercontent.com/110513499/183623207-d282f453-4c9b-4505-bad1-d680b5570774.png)

 Enabled techniques:-
 ![12_changes_improve_slack](https://user-images.githubusercontent.com/110513499/183623035-7cb39624-ab92-4cb8-8c12-b0468d05d1e3.png)
 
 Slack after using strategies:-
 ![14](https://user-images.githubusercontent.com/110513499/183623149-d02d9e33-a1ee-4a56-a98c-dda96d2486e0.png)
 
### Manually reduce slack
If after synthesis, while checking STA report if you find any cell causing huge delays you can manually try to resolve it. First, find the reason for the delay, if it is high fanout then it causes output load to increase and in turn increases delay. To solve this error manually replace the cell with a higher drive strength. Example is shown below

 Cell with 33 fanouts:-
 ![tmp](https://user-images.githubusercontent.com/110513499/183625302-e8456136-8703-457e-a752-c13a54128ffe.png)
 
 To increase drive strength use command replace_cells:-
 ![17_report_cells](https://user-images.githubusercontent.com/110513499/183625677-b8521241-89ee-4981-a9cc-e10ec547c5ae.png)
 
 Reduction in that cell delay:-
 ![18_changes__due_replace_cells](https://user-images.githubusercontent.com/110513499/183625849-8e41e068-1acc-4161-906c-27a672276e0d.png)
  
 ### How to run cts
 To run cts use command run_cts.
![run_cts](https://user-images.githubusercontent.com/110513499/183626679-b46abc38-c696-4560-82b9-5a170b6e9496.png)
  
## Day5

### Generation of Power Distribution Network (PDN)
 - To generate pdn, use command below command after cts:
      gen_pdn

The image below shows the run of pdn:
 ![1_pdn](https://user-images.githubusercontent.com/110513499/183630527-1b8f810d-f47d-4926-8704-dd8c77af138e.png)

### Output of pdn
 At the terminal, the details of the metals of power distribution is listed at the end of the execution. The image below shows it.
  ![2_PDn_info](https://user-images.githubusercontent.com/110513499/183630734-2212a0da-0364-41d9-b517-bd4f81a79c3f.png)
  
### Running routing
 In the openLane flow, routing is software used is Triton route. It does global routing as well as detailed routing. The below command runs it.
 ![3_run](https://user-images.githubusercontent.com/110513499/183631212-f354b9b2-3c1e-46ba-a528-aa4c0a85409d.png)


  
  
  
  
  
  






