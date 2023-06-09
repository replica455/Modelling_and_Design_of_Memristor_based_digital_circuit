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



!UPDATING SOON!
