# ADVANCED PHYSICAL DESIGN USING SKY130
The workshop has given overall idea on RTL to gds flow with help of openLANE eda tools and by using sky130 process technology, the design which is used in this workshop is picorv32a.


##TABLE OF CONTENTS
->DAY1 - INCEPTION OF OPEN SOURCE EDA,OPENLANE AND PDK
->DAY1 LAB
->DAY2-GOOD FLOORPLAN VS BAD FLOORPLAN AND INTRODUCTION TO LIBRARIES
->DAY2 LAB
->DAY3-DESIGN LIBRARY CELL USING MAGIC LAYOUT AND NGSPICE CHARECTERIZATION
->DAY4 - PRE LAYOUT TIMING ANALYSIS AND IMPORTANCE OF GOOD CLOCK TREE
->DAY4 LAB
->DAY5 - FINAL STEPS FOR RTL TO GDS AND ROUTING ALGORITHM
->DAY5 LAB




##INCEPTION OF OPEN SOURCE EDA AND PDK

QUAD flat no 48 

![image](https://user-images.githubusercontent.com/123498256/215535394-94a901d1-444d-4f77-8b76-3be41442cb1c.png)
chip:

pads on chip act like gate, through which signals can enter inside core area and different componets like IP's memory, analog to digital and digital to analog converters exist
foundry is the place where actually chip gets and manufactured

IP's & macors are distinguished, IP's are intelligence property and macros's are digital logic.

RISCV-ISA: it is used to communicate with computer, by converting assembly lanhuage to binary format to communicate with hardware.

PDK: process design kit is nothing but collection of files used to model fabriication process for the EDA tools used to design an IC, which consists of process design rules, device models, digital standard cell libraries, I/O libraries








DIGITAL ASIC DESIGN


![image](https://user-images.githubusercontent.com/123498256/215540896-5d2e00c1-c1e1-4318-bb53-c77d8760839d.png)

PnR flow:

synthesis->floorplan->powerplanning->placement->cts->routing


synthesis: it converts RTL to circuit out of components from the standard cell library


LAB:

![image](https://user-images.githubusercontent.com/123498256/215542159-9a2415fe-e1ff-4d55-8f05-da8ab529eaab.png)
\


![image](https://user-images.githubusercontent.com/123498256/215542282-060f8495-e5b6-4256-9dbd-b8dbfe4b4fec.png)



###DAY2  GOOD FLOORPLAN VS BAD FLOORPLAN:

FLOORPLAN: Partition the chip die between different ssystem building blocks and place the I/O pads and macros (dimensions, pin locations, row definition)

utilization factor: area of cells /total area of core

aspect ratio: h/w and if aspect ratio is one it is of square shape.


steps to run floorplan:

![image](https://user-images.githubusercontent.com/123498256/215545082-81bce303-345d-472c-9572-8e7a40025c9f.png)


tapcell: are used to connect n-well to avoid vdd and substrate to gnd(vss), this is to avoid latchup effect in cmos:


placement: at this stage, standard cells were placed and it follows two steps , one is globla placement and detailed placement,detailed placement is where cells are legalized so that cells will not be overlapped

Library not only has information of standard cells but also different sizes of cells of same gate which has different functionality and different vt cells



LAB:

![image](https://user-images.githubusercontent.com/123498256/215546334-090a7aad-2e4f-4ee0-b7a7-fee071f79380.png)





![image](https://user-images.githubusercontent.com/123498256/215546417-262c8d7b-54f9-4e9b-8a09-7efbca884346.png)





preplaced cells:



![image](https://user-images.githubusercontent.com/123498256/215546520-f7157adb-1bd5-4093-9fcc-e440138eaf90.png)




placement:

![image](https://user-images.githubusercontent.com/123498256/215546846-17904081-b3f7-4400-b4c7-4f7f94336c76.png)



![image](https://user-images.githubusercontent.com/123498256/215546925-361e7c6a-833a-4633-997c-d2233116b25c.png)



####day3 LAB:

![image](https://user-images.githubusercontent.com/123498256/215547331-1854f210-fe87-4c4e-9986-ece8295fc708.png)



![image](https://user-images.githubusercontent.com/123498256/215547405-78710ce3-4cd8-4a5f-851b-7fb7c7c00578.png)



layout of inverter:

![image](https://user-images.githubusercontent.com/123498256/215547508-73dfcdd4-2dc7-4151-ae5e-6ebbe581213f.png)



#####TIMING ANALYSIS AND IMPORTANCE OF GOOD CLOCK TREE:




LAB:



![image](https://user-images.githubusercontent.com/123498256/215552776-a73ecdfd-5e31-42d3-a178-2f2d0a2327e1.png)



![image](https://user-images.githubusercontent.com/123498256/215552892-1181a32a-186d-4421-8d1a-afb22aa69bea.png)



![image](https://user-images.githubusercontent.com/123498256/215553012-4799ca91-bb67-4bda-a7fb-c442d0311d49.png)



init_floorplan:

![image](https://user-images.githubusercontent.com/123498256/215553111-de964a1c-d45d-4507-8639-16c41abeb776.png)



![image](https://user-images.githubusercontent.com/123498256/215553226-6f1a32bf-e020-4d5d-bc56-63d0f7820129.png)



![image](https://user-images.githubusercontent.com/123498256/215553309-7eb8185d-1c3c-43e2-ae04-530012ba8fd0.png)






![image](https://user-images.githubusercontent.com/123498256/215554783-decde694-e0c0-4a28-b34d-224bfc101ff5.png)






![image](https://user-images.githubusercontent.com/123498256/215554832-5115b3eb-ea00-46c8-9ba4-4215bcf5c2e7.png)





######power distribution network and routing:

routing :where actual physical connection takes place at this stage and it is done in two phases ,one is global routing and the other is detailed routing

lee's algorithm :

![image](https://user-images.githubusercontent.com/123498256/215555215-59c49ebd-3788-4c07-a20d-594291848942.png)




















































