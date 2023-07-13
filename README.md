## Modelling_and_Design_of_Memristor_based_digital_circuit
### M. Tech Thesis work, University of Hyderabad 
### Thesis By - S. B. Acharyya
### Guided By - 


 ![Dr-S-V-S-Nageswara-Rao-p43ghfjwh8y5433ivq6hzw7snovn4149ubl4k0mbbg](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/3aa19767-52ea-468d-898f-842154e75900)

### Prof. Nageswara Rao S. V. S.
* Designation Professor (12/2016 – to date)
* Personal web page	https://scholar.google.co.in/citations?user=P2ko_TUAAAAJ&hl=en
* Qualification	Ph.D. (University of Hyderabad)
* Phone: +91 +914023134329
* E-mail: svnsp@uohyd


# Introduction 

*  circuits built with semiconductor 
devices have provided significant growth in the number of processing elements and 
memory bits available to system developers. This growth has provided orders of 
magnitude improvements in speed, power consumption, and reliability, together with 
significant reductions in the cost per device
* These trends are direct consequences of 
frequent miniaturization of device dimensions in the semiconductor fabrication 
process, as originally described by Gordon Moore in 1965, predicting the growth and 
proliferation of digital computing and its applications ("Moore's Law")
* Moore's law, however, cannot be sustained indefinitely
* CMOS transistor sizes will reach fundamental physical limits within 
the next decade
* the field of computing is already struggling with other 
fundamental problems which require innovative solutions. The first problem is related 
to the delay and bandwidth required to access memory, and is popularly known as 
"the memory wall" 
* Another problem is the power crisis related to energy 
dissipation in computers 
* In future years, when device sizes will no longer be scalable, microelectronic 
technology will need innovations "beyond Moore" to support novel applications. 
* An example of a "more than Moore" 
technology is multi-layered integrated circuits (e.g., three-dimensional circuits 
* Other new technologies which will 
extend the capabilities of CMOS are memristive devices. This thesis focuses on 
memristive technologies and their impact on computers.

# Memristor 
* Flash memory based on charge trapping in MOS transistors 
* Scaling below 20 nm 
involves formidable challenges, particularly an increase in bit error rate and a 
reduction in write endurance (the number of write cycles before the memory becomes 
unreliable).
* In recent years, many alternative technologies have been 
explored to find a replacement for flash. For most of these candidate technologies, the 
stored data is represented as a resistance and the storage device is fabricated within 
the metal layers.
* These technologies share similar properties – nonvolatility, relatively 
high write endurance, high density, good scalability below 10 nm, and fast read and 
write
```
These emerging nonvolatile memory technologies can be 
considered as memristors, or more precisely as memristive devices
```

# Memristor Theory

* four fundamental circuit variables - the voltage V, current I, flux φ, and electric charge q.
* ![Two-terminal_non-linear_circuit_elements svg](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/e25407d0-adc9-4ba9-85a6-4d38db080e13)
* Resistors connect voltage to current by Ohm's law (V = IR), capacitors connect charge to 
voltage (q = CV), and inductors connect current to flux (φ = LI). 
* possible 
relationship is the connection between charge and flux and is not covered by any 
conventional circuit element.
* for the sake of completeness, the 
existence of a fourth fundamental circuit element that connects the charge and flux 
and named the device the ```memristor```, as a short for ```memory resistor```.
* Formally, a charge-controlled memristor is given by ```v(t) = M(q(t)) i(t)``` where  " M " is called memristance of memristor defined by ``` M(q(t)) = dφ(q)/dq ```
* The above relations can be summarised like this


 
 ![1](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/ff4c5c3b-6852-4c4d-a4ad-1069e5dcd830)
* The memristance of the memristor  has the units of resistance
* The memristor is therefore actually a passive two-port 
element with variable resistance, which changes upon the history of the device (i.e., 
the memristance depends on the total charge passed through the device)
* In 1976, the theory of memristors was extended by Chua and Kang to a nonlinear 
dynamical system named memristive systems
* Similarly to memristors, a 
memristive device is a passive two-terminal device with varying resistance
* The difference between a memristor and memristive device is how the resistance changes. 
In memristive devices, the resistance depends on an internal state x ∈ R^n, which 
depends on the history of the device (in terms of the past current passed through the 
device, or, alternatively, the past voltage across the device) and not directly on the 
charge
* Memristors and memristive devices exhibit hysteresis in their current-voltage curve.
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/30aae993-9c02-487e-b020-ed1833f53879)
* Although the shape of the hysteresis varies for different devices, it is always passes 
through the origin. The hysteresis depends on the input, where for high input 
frequencies the device behaves as a linear resistor
* v = M(x).i --> i=0 --> v=0 : zero crossing
“if it’s pinched, it’s a memristor” (L.Chua)
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/ac92faee-f1a1-4d42-8605-acd3f23fb80b)
  


# Practical Memristors 

* Hewlett Packard 
connected the theory of memristive devices to TiO2 resistive switches
*  Initially, 
Hewlett Packard claimed that their device is similar to ideal memristors, and proposed 
a model for the structure and behavior of their devices
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/e7619060-b885-428e-8131-49d3a6db33c1)
* He modelled the memristance as ``` M(x,i) = [ Ron (x(t) / D) ] + [ Roff (1 - {x(t)/D})] ``` 
* where RON is the resistance when x(t) = D, and ROFF is the resistance when x(t) = 0. 
The state variable x(t) is limited to the physical dimensions of the device, i.e., the 
value is within the interval [0, D].
* Now why and how the " x " is actually a variable stste model of device can be understood like - Just like previous structure of doped and undoped TiO2 we can represent it more specifically as 
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/e18393dc-a404-4bfc-99b2-213280ca8dac)
* The structure of TiO2 is little complicated to understand but anyway here is the structure 
* ![Rutile-unit-cell-3D-balls](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/8ef63377-cdc9-43dc-a8bf-beab60f143c0)
* TiO2 is usually an electrical insulator but when some of O2 ions are missing this can lead to electrical conductivity. This can be illustrated by following diagram. For the sake of simplicity I've removed the covalent bond between Ti+ and O- ions. 
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/71832692-77f6-4937-999a-bb373d5ee56c)
* Remember that the oxygen is a negatively charged ions so it will move gainst the direction of electric field. the resi of diagram is self explainatory.
* Now remember the platinum metal electrodes of the device, You have to create potential difference across the TiO2 layer 
* The vacancied can be represented as positive charges. Obviously the doped region can be represented to have lot of vacancy. The undoped region has no vacancy. So now pictirically representing it like the figure I made -  
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/469ae595-8455-42cf-be4e-0e60e7aaa28e)
* Now remember the current can flow due to the vacancies i.e. the doped TiO2 plays the role for current flow
* Let you have applied the positive potential at top Pt electrode and Negative potential at bottom electrode. In this case the same amount of positive vacancy is reppled by positive potential, So we can say the same amount of positive charges are now distributed more into undoped region i.e. the variable factor " x " has now greater value. Now in this state the Film as a whole is more conductivei.e. resistance is small. Now this can also be compared to forward biasing. Same has been illustrated by the diagram
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/9fe4b3f0-b27a-4d19-bc56-104e6cf07f58)
* Similarly If you reverse the potential the reverse thing will happen. The positive charges will now remain more confine to doped region and variable "x" will become smaller. Ther overall conductance will reduce and resistance will increase. This can be illustrated by following diagram 
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/9511462c-7d3f-4986-bef6-863cf8a484e3)
* Note that In both of the case the number of vacancy remains same.
* So by changing the potential we are changing the depletion region, which in turn changes the resistance of film which in turn changes the conductance of the film.
* In any time the potential is removed then the depletion region width i.e. "x" value do not changes i.e. it remains to lase state it was in thus producing a memory condition for the device.

# Why Hysteresis ?
The current-voltage (I-V) characteristic of a memristor is typically represented by a butterfly hysteresis loop. This is because the resistance of a memristor depends on the direction and magnitude of the current that has passed through it, and these effects are cumulative over time. As a result, the I-V characteristic of a memristor shows a hysteresis loop that resembles the shape of a butterfly.

***Let us now eleborate***

now from the previous discussion we already know by applying potential on the top and bottom electrode the oxygen vacancies may intrude in the undoped region or may remain confined to the doped region which will make the low resistance (high conductance) path or high resistance (low conductance) path i.e. the resistive syitching occurs. In very simple manner we can depict the mechanism as the diagram as shown below


![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/53761522-c654-458e-8124-c21e85399da2)


See we have introduced some standard terminilogy. when the Resistance is low (LRS) i.e. the oxygen vacancies intrude deep into the undoped region and touches the bottom electrode (filament has formed) the current can easily frow through the device and this is called the ***SET*** state.
Similarly at high resistance state (HRS) the current cant frow through the device and this state is called the ***RESET*** state. From The perspective of digital electronics it can be shown like the picture below. the LRS is equivalent to ligic 1 and HRS is equivalent to logic 0.

![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/8d89d90d-953f-4f98-a1f7-b78b7860f2a1)

Now finally coming to the IV characterestics. First we have to know what is the difference between IV of resistor and memristor. When  it comes to resistor we know there is no resistive switching phenomena i.e. if a resistor has a rasistance of 10Kohm it will stay at 10Kohm whatever permisible amount of voltage is applied  so quite obviously the IV character is a straight line passing through the origin. 
Now thing is different in case of memristor. Let us go step by step

* First there was no voltage applied to the device and we keep on increasing the voltage from V=0 gradually. So as the voltage applied is small the filament of oxygen vacancies didn't formed properly the device remain in HRS, i.e. by applying the voltage we are getting only small amount of current. You can follow the picture that our device is in HRS.

![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/9c66cb40-c8df-4597-a37a-f53d1bd83713)

* Now as the voltage increases beyond a particular point the filament is formed completely and the current flow increases and our device switches to LRS. That particular voltage is termed as Vset. the picture looks like this below where the Ic compliance current set to limit the potentially very high current during set process.

![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/f2af6dab-9151-4479-99ee-52c137cb8835)


* Now if you start to reduce the voltage at particular negative value you will get the current suddenly becomes close to zero, so we can conclude the filament has been raptured. This particular case is back again to HRS, whiv=ch will bring us back to blue line. Overall the IV character looks like this


![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/c514330f-9904-484f-bef6-9992b617c493)







# Typical Memristor device Character 

All of the different devices that can be considered as memristive devices share 
several characteristics
*  They are fabricated as oxides sandwiched between two metals 
(metal-insulator-metal structure, also named MIM)
* their size is relatively small 
(for most devices it is the minimum feature size of the technology)
*  Additionally, as 
described by the definition of memristive devices, these devices have varying 
resistance and are nonvolatile (i.e., no voltage is applied to retain the resistance)
* their relatively low switching time (from sub-nanoseconds 
to tens of nanoseconds)
* high endurance (the number of write cycles before the 
memory becomes unreliable, typically from 109 to 1015)
* low switching energy 
(typically 0.1 to 1 pJ)
* memristive technologies are primarily investigated as memory 
applications and considered as emerging nonvolatile memory technologies
* It is common to refer all (or some) of these technologies as Resistive RAM (RRAM or 
ReRAM).

# Speciar summary Point on Memristor
* It is a 2 terminal non-linear resistor
* It is a passive element and doesnot store energy
* It remembers last amount of current passed through it or last value of voltage applied to it
* It is resistor with a memory
* Non-linear relationship between voltage and current
* No phase shift introduced between current and voltage at zero crossing
* I-V character is a pinched Hysterisis Loop which is a function of applied frequency 
* Physically it was develloped like Pt-TiO2-Pt (M-I-M) layer device.

# Memristor Circuit point of view
So far we know memristor is a passive device. Our target is to use it in circuits. For that we need to look at the polarity of the device. The thick black line in memristor symbol represents the polarity of the device. When current enters the blsck mark then the resistance decreases to Ron . Similarly when the current leaves the mark then the device shows high resistance Roff. 
* The basic boolean logic operations AND and OR can be analysed using memristors.
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/8cdf388a-d15d-4680-b01f-3b47ab6eb347)
* The following set of figure describes the computation of AND operation for allinput cases of a two input AND gate using memristors only.
###  AND OPERATION - A=1 B=1
* For case A=1 and B=1, both the inputs are tied to VCC i.e., at logic 1. As described in below figure, no current flow through the circuit and the output in this case is logic = VCC or 1.
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/f6edeb4f-0e28-40c8-9a36-953c94655c2b)
###  AND OPERATION - A=0 B=0
* For the case of A=0 and B=0 as shown in below figure it can be considered that the inputs are at logic 0, the output should also be logic 0. Again there is no current flow through the circuit, the same logic appears at output node Y
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/70ac31f0-257c-43fe-b7d3-5aabe6b5bc60)
###  AND OPERATION - (A=1 B=0) OR (A-0 B=1)
*For the case when any of input is at logic 1 and other at logic 0 as shown in below figure. In this case, input A=1 and B=0 the current flows through VCC to GND. When current passes from memristor MR0, the resistance of that memristor increases to Roff, the resistance of memristor MR1 decreases to Ron and current leave through GND node. Resistance of memristors are ROFF >>> RON. By this way, we get two resistors ROFF and RON with different values. Thus as per the voltage divider rule, we get The calculation of output voltage at Y for the voltage divider
 circuit can be determined as
```
 Y = VCC * [RON / (RON +ROFF)]
 ROFF is significantly higher than RON we can simplify the equation as
 Y =VCC * (RON / ROFF) << VCC
 Y ~ GND
 ```
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/df9a209a-0755-425e-a447-5017b5eb538d)

### OR gate operation 
* When the polarity of the memristors MR0 and MR1 is reversed, the circuit behaves as OR gate, and its analysis can be done is similar way.
* For inputs A=0,B=0 and A=1,B=1 the output Y get the value 0 and 1 as no
 current flow through the circuit and the behavior remains same
 as in the case of AND gate.
* In below figure shows the case when any one of the input is at logic 1 and other at logic 0. Current flows through the VCC towards memristor MR0. As the memristor is in reverse polarity arrangement, the resistance of the memristor decreases to RON and thus the voltage shows up at output node Y=VCC. The output becomes logic 1 when any of the input is at logic 1. The resistance of other memristor MR1 increases to RON and the condition remains same ROFF>>>RON because these are the fixed values. The output can be determined for
 OR gate using the voltage divider rule as
``` Y =VCC * [(ROFF / RON +ROFF )] ~ VCC```
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/563d176d-8b3b-4c75-beb2-eebb2923674a)
  
### Comments
AND and OR gates can be implemented using memristors only. By this topology, even ‘n’ input gates can be implemented using memristors.
### Inverter Operation
 But the primary issue is incomplete
 logic family. Without NOT operation, it is not possible to
 implement boolean functions. Not Gate uning only memristor is not possible at all. So CMOS inverter can be used to
 implement NOT operation. So if CMOS inverter is designed using 180 nm process technology. The operating voltage for the CMOS inverter is 1.8 V. We kept the same parameter of memristors as used to simulate the current–voltage

### Universal Gate Implementation

As describedinprevious section, NOT operation is not possible with memristors. So, to get the complete logic family we should add CMOS inverter at the output ofAND gate to get NAND operation and similarly NOR operation can alsobe implemented. The below diagram is of NAND gate.


![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/fc72821e-2107-4349-91ab-084b80113c28)

## Other logic gate and combinational circuits

### !UPDATING SOON!

## Neuromorphic Computating using Memristor

### Motives and background

* In conventional Von-Neumann architecture the CPU and Memory are placed separately which can lead to data congestionin data bus due to data movement. This situation is called memory bottle neck.
* In our Human brain anatomy there is no segrigation between memory storage location and computation area, all as a whole we recognize as brain and among them specifically we see the neural network composed neurons, axions, synapse etc.
* Considering the anatomy of brain we improvise the neuromorphic computing or in memory computaion where the system can be imagined as homogenous set of nodes which are connected to each other is a grid or matrix format where a particulat node can be used as storage element or an computation element according to necessity.
* This grid or matrix structure is implemented as hardware in form of  crossbar architecture
* This crossbar architecture provides a high sense of parallism in computation and storage
* The storage and computation element can be develloped using the memristor we have discussed so far.
* This whole arrangement of memristor in a crossbar arrangement is called Resistive RAM (RRAM)
* ![neu_cross](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/270e1fcd-2abb-4cad-b444-1405055b92a0)

### RRAM
There are some features which i would like to summarise in short
* The RRAM are Nonvolatile in nature
* They can store the data in form of resistance
* Unlike CMOS the in memory computation dosnot favour heteroginity of logic primitive. So basically we need to think about functionally complete logic like (NOR), (NAND), (Majority detector + NOT), (Imply + FALSE). So stick to particular logic only if you are implementing the gates using nor gate then stick to nor gate only.
* The main mechanism for switching of oxide based RRAM is the formation and rupture of a conductive
filament. These are formed by applying a soft breakdown voltage over the device. Initially the RRAM
is at a high resistance state (HRS). To get a working RRAM cell, a filament is constructed by a forming
voltage. The electric field displaces oxygen ions, which reside in the dielectric, towards the oxygen rich
region, leaving a conductive oxygen vacancy filament. In this mode the RRAM is said to be in a low
resistance state (LRS). To reset the RRAM into a HRS a reverse bias is applied which lets the oxygen re-migrate into the filament, resulting in a rupture. A set operation can be programmed by
again applying a positive voltage. The mechanism can be understood with following diagram
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/93a99692-08aa-4c91-b7da-c7deab8fe2c6)
* The CBA is a square array with the rows and columns separated by
RRAM cells, situated on each node
* Ideally, passive CBAs would
stand as an excellent structure, though the operations that are used to write and read memory bring
difficulties related to leakage currents.
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/e2d3340b-2987-4250-8224-ccc4b9104589)
* Active CBAs have been shown to suppress leakage currents by introducing selector devices in the
cell. The selectors are coupled in series with the RRAM. In particular the one-transistorone-RRAM (1T1R) structure will be investigated.
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/a76f4185-25ed-4847-b744-718a57ef39bc)
* A cell is programmed by applying voltages to the word-line (WL) and bit-line (BL) of the CBA. The
WL connects to a row of cells. The operation is trivial for passive CBAs but for 1T1R CBAs the WL
accesses the transistor and allows for a current to flow between the source and the drain. The specific
way the WL and BL are biased depends on the type of CBA.
* So along with the control line the passive RRAM looks like the figure below
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/750b12cf-75ea-4da2-88cc-8ae8d51024fc)
* And along with the control line the active aRRAM looks like the figure below
* ![image](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/5eecc5fe-c395-4faf-a60e-a4f865c92b2a)
* So now in a broad sense the 1T-1R RAM can be pictured like the figure below
*  ![3-Figure2-1](https://github.com/replica455/Modelling_and_Design_of_Memristor_based_digital_circuit/assets/55652905/6f3ee048-b744-40d2-b67a-79714e4d487f)
*  The SL are the source line which remains grounded.
*  










# Reference 

* Memristor-Based 
Circuits and 
Architectures 
Research Thesis 
In Partial Fulfillment of the Requirements for the 
Degree of Doctor of Philosophy 
Shahar Kvatinsky 
Submitted to the Senate of the 
Technion – Israel Institute of Technology
* Memristor-Inspired Digital Logic Circuits and
 Comparison With 90-/180-nm
 CMOSTechnologies by, Sanjay Kumar, Member, IEEE, Mohit Kumar Gautam
* https://www.youtube.com/watch?v=4dfGm7zkTiM
* https://www.youtube.com/watch?v=NxfZ9JXm1Qw
* Wikipedia memristor article
* Hybrid Memristor-CMOS (MeMOS) based Logic Gates and Adder Circuits Tejinder Singh, Member, IEEE
* https://www.youtube.com/watch?v=jTX3EHHFM5s
* Thesis for Master’s Degree in Physics
Investigation of Resistive Random Access
Memory for 1T1R Nanowire Array
Integration
Autumn 2019 - Spring 2020
LUND UNIVERSITY FACULTY OF SCIENCE

# Special Vote of Thanks

* Dr. S.V.S Nageshwar Rao, Ph.D. (University of Hyderabad) (GUIDE)
* Sai Prasad Goud (Research scholar University Of Hyderabad)
* Dr. Sanjay Kumar, Ph.D (IIT Indore) 

