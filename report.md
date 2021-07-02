<html>
<head><meta http-equiv=Content-Type content="text/html; charset=UTF-8">
<style type="text/css">
<!--
span.cls_002{font-family:Arial,serif;font-size:14.0px;color:rgb(66,66,66);font-weight:normal;font-style:normal;text-decoration: none}
div.cls_002{font-family:Arial,serif;font-size:14.0px;color:rgb(66,66,66);font-weight:normal;font-style:normal;text-decoration: none}
span.cls_003{font-family:Arial,serif;font-size:11.1px;color:rgb(0,0,0);font-weight:normal;font-style:normal;text-decoration: none}
div.cls_003{font-family:Arial,serif;font-size:11.1px;color:rgb(0,0,0);font-weight:normal;font-style:normal;text-decoration: none}
span.cls_004{font-family:Arial,serif;font-size:12.1px;color:rgb(102,102,102);font-weight:normal;font-style:normal;text-decoration: none}
div.cls_004{font-family:Arial,serif;font-size:12.1px;color:rgb(102,102,102);font-weight:normal;font-style:normal;text-decoration: none}
span.cls_005{font-family:Arial,serif;font-size:11.1px;color:rgb(0,0,0);font-weight:bold;font-style:normal;text-decoration: none}
div.cls_005{font-family:Arial,serif;font-size:11.1px;color:rgb(0,0,0);font-weight:bold;font-style:normal;text-decoration: none}
-->
</style>
<script type="text/javascript" src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/wz_jsgraphics.js"></script>
</head>
<body>
<div style="position:absolute;left:50%;margin-left:-306px;top:0px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background01.jpg" width=612 height=792></div>
<div style="position:absolute;left:216.00px;top:109.83px" class="cls_003"><span class="cls_003">Traffic Light System</span></div>
<div style="position:absolute;left:180.00px;top:138.92px" class="cls_003"><span class="cls_003">Report Authored By: Muhammad Asim Ali</span></div>
<div style="position:absolute;left:216.00px;top:168.02px" class="cls_003"><span class="cls_003">Date: March 16, 2021</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:802px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background02.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.13px" class="cls_002"><span class="cls_002">Introduction</span></div>
<div style="position:absolute;left:72.00px;top:108.38px" class="cls_003"><span class="cls_003">The Traffic Light System project simulates traffic on a one-way, one-lane road with an</span></div>
<div style="position:absolute;left:72.00px;top:122.92px" class="cls_003"><span class="cls_003">intersection that has a single traffic light. In this project LED’s are used to represent lights and</span></div>
<div style="position:absolute;left:72.00px;top:137.47px" class="cls_003"><span class="cls_003">vehicles and a potentiometer is used as an input device to determine the rate at which traffic is</span></div>
<div style="position:absolute;left:72.00px;top:152.02px" class="cls_003"><span class="cls_003">generated in the simulation. Figure 1 below taken from the ECE 455 Lab Manual shows the</span></div>
<div style="position:absolute;left:72.00px;top:166.56px" class="cls_003"><span class="cls_003">user interface for the simulation.</span></div>
<div style="position:absolute;left:72.00px;top:341.63px" class="cls_003"><span class="cls_003">Figure 1 - User interface of the Traffic Light System simulation</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:1604px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background03.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.13px" class="cls_002"><span class="cls_002">Initialization of the middleware</span></div>
<div style="position:absolute;left:72.00px;top:103.77px" class="cls_004"><span class="cls_004">Overview</span></div>
<div style="position:absolute;left:72.00px;top:123.70px" class="cls_003"><span class="cls_003">Pins PC0-PC6 were used for this project. PC0-PC2 were configured as output pins, these pins</span></div>
<div style="position:absolute;left:72.00px;top:138.25px" class="cls_003"><span class="cls_003">were used by the application code to display the traffic light state. For example if the current</span></div>
<div style="position:absolute;left:72.00px;top:152.79px" class="cls_003"><span class="cls_003">traffic light state was red then PC0 would have a high output signal indicating that the red light</span></div>
<div style="position:absolute;left:72.00px;top:167.34px" class="cls_003"><span class="cls_003">was turned on. Pin PC3 was configured as an analog input pin to receive the potentiometer</span></div>
<div style="position:absolute;left:72.00px;top:181.89px" class="cls_003"><span class="cls_003">input. PC6-PC8 were the pins associated with the shift register. The shift register (serial in</span></div>
<div style="position:absolute;left:72.00px;top:196.43px" class="cls_003"><span class="cls_003">parallel out) was used to provide output to 19 leds which when active each represent the</span></div>
<div style="position:absolute;left:72.00px;top:210.98px" class="cls_003"><span class="cls_003">location of a vehicle in the simulation.  The figure below taken from the ECE 455 Lab Manual [1]</span></div>
<div style="position:absolute;left:72.00px;top:225.52px" class="cls_003"><span class="cls_003">shows a list of the port pins used and their associated functionality.</span></div>
<div style="position:absolute;left:108.00px;top:387.55px" class="cls_003"><span class="cls_003">Figure 2 - Pins used for this project with their associated functionality</span></div>
<div style="position:absolute;left:72.00px;top:430.58px" class="cls_004"><span class="cls_004">Software Setup : GPIO Pins</span></div>
<div style="position:absolute;left:72.00px;top:450.51px" class="cls_003"><span class="cls_003">The STM standard peripheral drivers were used to initialize the GPIO and ADC for this project.</span></div>
<div style="position:absolute;left:72.00px;top:465.06px" class="cls_003"><span class="cls_003">The peripheral drivers provide the convenience of not directly having to write to registers.</span></div>
<div style="position:absolute;left:72.00px;top:479.60px" class="cls_003"><span class="cls_003">Instead to initialize a GPIO pin an struct is provided by by the driver to configure the GPIO pin</span></div>
<div style="position:absolute;left:72.00px;top:494.15px" class="cls_003"><span class="cls_003">settings.</span></div>
<div style="position:absolute;left:72.00px;top:523.24px" class="cls_003"><span class="cls_003">Some of the settings are detailed below:</span></div>
<div style="position:absolute;left:72.00px;top:552.33px" class="cls_005"><span class="cls_005">GPIO_MODE</span><span class="cls_003"> - This sets the mode of the pin, it can be set to input, output, analog and other</span></div>
<div style="position:absolute;left:72.00px;top:566.88px" class="cls_003"><span class="cls_003">modes.</span></div>
<div style="position:absolute;left:72.00px;top:581.43px" class="cls_003"><span class="cls_003">In this project PC0-PC2 and PC6-PC8 corresponding to the traffic light LED’s and shift register</span></div>
<div style="position:absolute;left:72.00px;top:595.97px" class="cls_003"><span class="cls_003">were set to output mode. PC3, corresponding to the potentiometer input was set to Analog</span></div>
<div style="position:absolute;left:72.00px;top:610.52px" class="cls_003"><span class="cls_003">(ADC).</span></div>
<div style="position:absolute;left:72.00px;top:639.61px" class="cls_005"><span class="cls_005">OTYPE</span><span class="cls_003"> - This specified the output type with choices from open drain and push pull.</span></div>
<div style="position:absolute;left:72.00px;top:654.16px" class="cls_003"><span class="cls_003">PushPull was selected for all in the GPIO pins as it appears to be the standard where a low</span></div>
<div style="position:absolute;left:72.00px;top:668.70px" class="cls_003"><span class="cls_003">corresponds to the signal being pulled to ground and a high corresponds to the signal being</span></div>
<div style="position:absolute;left:72.00px;top:683.25px" class="cls_003"><span class="cls_003">pushed to high. [2]</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:2406px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background04.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.32px" class="cls_005"><span class="cls_005">PuPd</span><span class="cls_003"> - The pul down/ pull up settings prevent floating values from occouring by adding a</span></div>
<div style="position:absolute;left:72.00px;top:85.86px" class="cls_003"><span class="cls_003">resistor either to VCC or GND.</span></div>
<div style="position:absolute;left:72.00px;top:100.41px" class="cls_003"><span class="cls_003">Pull Down was used for PC0-PC2 and PC6-PC8 corresponding to the traffic light LED’s and the</span></div>
<div style="position:absolute;left:72.00px;top:114.96px" class="cls_003"><span class="cls_003">shift register. Pull down means that when there is no high signal the state of the signal will be</span></div>
<div style="position:absolute;left:72.00px;top:129.50px" class="cls_003"><span class="cls_003">guranteed to be low. For the ADC pin no pull was selected.</span></div>
<div style="position:absolute;left:72.00px;top:158.60px" class="cls_005"><span class="cls_005">SPEED</span><span class="cls_003"> - This affects the rise time and fall time of the output.</span></div>
<div style="position:absolute;left:72.00px;top:173.14px" class="cls_003"><span class="cls_003">Options from 2MHz to 100 MHz are available. 2MHz proved to be sufficient for the purpose of</span></div>
<div style="position:absolute;left:72.00px;top:187.69px" class="cls_003"><span class="cls_003">this project for all of the GPIO pins.</span></div>
<div style="position:absolute;left:72.00px;top:216.17px" class="cls_004"><span class="cls_004">Software Setup: ADC initialization</span></div>
<div style="position:absolute;left:72.00px;top:236.10px" class="cls_003"><span class="cls_003">To initialize the ADC the GPIO pin PC3 was initialized as an Analog pin with no Pull followed by</span></div>
<div style="position:absolute;left:72.00px;top:250.65px" class="cls_003"><span class="cls_003">the ADC specific settings. One of the settings initialized for the ADC was ADC_Resolution. This</span></div>
<div style="position:absolute;left:72.00px;top:265.20px" class="cls_003"><span class="cls_003">setting determines the precision of the input. 12 Bit precision was select which implies that a</span></div>
<div style="position:absolute;left:72.00px;top:279.74px" class="cls_003"><span class="cls_003">maximum of 4096 values can be used to represent the voltage input by the potentiometer.</span></div>
<div style="position:absolute;left:72.00px;top:308.83px" class="cls_003"><span class="cls_003">PC3 can be connected to ADC1, ADC2 and ADC 3. ADC 1 was selected for this project and it</span></div>
<div style="position:absolute;left:72.00px;top:323.38px" class="cls_003"><span class="cls_003">was connected with channel 13 with a sample time of 56 Cycles.</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:3208px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background05.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.13px" class="cls_002"><span class="cls_002">Software Design</span></div>
<div style="position:absolute;left:72.00px;top:108.38px" class="cls_003"><span class="cls_003">This project used:</span></div>
<div style="position:absolute;left:126.00px;top:122.92px" class="cls_003"><span class="cls_003">●</span></div>
<div style="position:absolute;left:144.00px;top:122.92px" class="cls_003"><span class="cls_003">3 queues</span></div>
<div style="position:absolute;left:162.00px;top:137.47px" class="cls_003"><span class="cls_003">○  XQueue_State</span></div>
<div style="position:absolute;left:162.00px;top:152.02px" class="cls_003"><span class="cls_003">○  xQueue_light_state</span></div>
<div style="position:absolute;left:162.00px;top:166.56px" class="cls_003"><span class="cls_003">○  xQueue_generate</span></div>
<div style="position:absolute;left:126.00px;top:195.66px" class="cls_003"><span class="cls_003">●</span></div>
<div style="position:absolute;left:144.00px;top:195.66px" class="cls_003"><span class="cls_003">4 tasks</span></div>
<div style="position:absolute;left:162.00px;top:210.20px" class="cls_003"><span class="cls_003">○  Traffic_state</span></div>
<div style="position:absolute;left:162.00px;top:224.75px" class="cls_003"><span class="cls_003">○  Display</span></div>
<div style="position:absolute;left:162.00px;top:239.29px" class="cls_003"><span class="cls_003">○  Traffic_generate</span></div>
<div style="position:absolute;left:162.00px;top:253.84px" class="cls_003"><span class="cls_003">○  Traffic_light_state</span></div>
<div style="position:absolute;left:72.00px;top:296.87px" class="cls_004"><span class="cls_004">Design Document</span></div>
<div style="position:absolute;left:72.00px;top:316.80px" class="cls_003"><span class="cls_003">The development of this project was a very iterative process.There were many “rough” design</span></div>
<div style="position:absolute;left:72.00px;top:331.35px" class="cls_003"><span class="cls_003">documents used. The design document below captures the gist of the design. One of the</span></div>
<div style="position:absolute;left:72.00px;top:345.89px" class="cls_003"><span class="cls_003">biggest challenges early in the development of this project was how the traffic state can be</span></div>
<div style="position:absolute;left:72.00px;top:360.44px" class="cls_003"><span class="cls_003">represented. After a few iterations an array was selected to represent the state of the traffic. A 1</span></div>
<div style="position:absolute;left:72.00px;top:374.99px" class="cls_003"><span class="cls_003">for an array index indicates that the LED at that index should be on and a 0 indicates it should</span></div>
<div style="position:absolute;left:72.00px;top:389.53px" class="cls_003"><span class="cls_003">be off. It was quite clear in the beginning that a queue would be required to send and receive</span></div>
<div style="position:absolute;left:72.00px;top:404.08px" class="cls_003"><span class="cls_003">the state of the traffic lights, the amount of new vehicles being generated and to the current</span></div>
<div style="position:absolute;left:72.00px;top:418.63px" class="cls_003"><span class="cls_003">state of the vehicles to the display task. A design difference from the beginning and the end was</span></div>
<div style="position:absolute;left:72.00px;top:433.17px" class="cls_003"><span class="cls_003">that the display middleware for the traffic lights was called directly from the traffic light task</span></div>
<div style="position:absolute;left:72.00px;top:447.72px" class="cls_003"><span class="cls_003">rather than the display task, this was done to avoid using yet another queue.</span></div>
<div style="position:absolute;left:72.00px;top:695.99px" class="cls_003"><span class="cls_003">Figure 3 - Design document</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:4010px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background06.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.26px" class="cls_004"><span class="cls_004">System overview diagram</span></div>
<div style="position:absolute;left:72.00px;top:91.19px" class="cls_003"><span class="cls_003">The following diagram provides an overview of the relationships between the tasks and queues</span></div>
<div style="position:absolute;left:72.00px;top:105.73px" class="cls_003"><span class="cls_003">used in the final version of this project.</span></div>
<div style="position:absolute;left:72.00px;top:463.51px" class="cls_003"><span class="cls_003">Figure 4 - System overview diagram showing the relationship between the tasks and queues.</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:4812px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background07.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:116.22px" class="cls_002"><span class="cls_002">Implementation details</span></div>
<div style="position:absolute;left:72.00px;top:138.92px" class="cls_003"><span class="cls_003">The discussion below summarizes the functionality of each of the tasks and queues.</span></div>
<div style="position:absolute;left:72.00px;top:167.41px" class="cls_004"><span class="cls_004">Task: traffic_light_state</span></div>
<div style="position:absolute;left:72.00px;top:203.21px" class="cls_003"><span class="cls_003">The traffic_light_state task is the highest priority task (priority =4) of the system. Based on the</span></div>
<div style="position:absolute;left:72.00px;top:217.75px" class="cls_003"><span class="cls_003">traffic flow (based on normalized ADC input) the task determines the amount of time to delay the</span></div>
<div style="position:absolute;left:72.00px;top:232.30px" class="cls_003"><span class="cls_003">current light. A variable titled “current_state” determines the light that is currently on</span></div>
<div style="position:absolute;left:483.18px;top:232.30px" class="cls_003"><span class="cls_003">(a value of</span></div>
<div style="position:absolute;left:72.00px;top:246.85px" class="cls_003"><span class="cls_003">2 corresponds to green, 1 corresponds to yellow and 0 corresponds to red). The task sends the</span></div>
<div style="position:absolute;left:72.00px;top:261.39px" class="cls_003"><span class="cls_003">“current_state” value over the “XQueue_light_state” queue and then suspends itself for the</span></div>
<div style="position:absolute;left:72.00px;top:275.94px" class="cls_003"><span class="cls_003">amount of time determined by the traffic flow rate and the “current_state”. The “amber light”</span></div>
<div style="position:absolute;left:72.00px;top:290.48px" class="cls_003"><span class="cls_003">(current_state=1) has a fixed delay time of 2000 ticks and the “green” and “red” lights</span></div>
<div style="position:absolute;left:72.00px;top:305.03px" class="cls_003"><span class="cls_003">(current_state =2 and 0 respectively) have their delay tick time determined by the following</span></div>
<div style="position:absolute;left:72.00px;top:319.58px" class="cls_003"><span class="cls_003">formulas:</span></div>
<div style="position:absolute;left:180.00px;top:348.67px" class="cls_003"><span class="cls_003">float greenTime = 10 + normalized_adc * 10;</span></div>
<div style="position:absolute;left:180.00px;top:377.76px" class="cls_003"><span class="cls_003">float redTime = 20 - normalized_adc * 10;</span></div>
<div style="position:absolute;left:72.00px;top:421.40px" class="cls_003"><span class="cls_003">The formulas dictate that at lowest traffic flow the red light time will be 20(double) and green</span></div>
<div style="position:absolute;left:72.00px;top:435.95px" class="cls_003"><span class="cls_003">light time will be 10 and vice versa at the highest traffic flow rate.</span></div>
<div style="position:absolute;left:72.00px;top:478.98px" class="cls_004"><span class="cls_004">Task: traffic_generate</span></div>
<div style="position:absolute;left:72.00px;top:498.91px" class="cls_003"><span class="cls_003">The “traffic_generate” task has the second highest priority (priority =3). This means that</span></div>
<div style="position:absolute;left:72.00px;top:513.46px" class="cls_003"><span class="cls_003">everytime the “traffic_light_state” task is suspended the “traffic_generate” task runs until it</span></div>
<div style="position:absolute;left:72.00px;top:528.00px" class="cls_003"><span class="cls_003">suspends its execution or it is pre-empted by the “traffic_light_state” task.  This task reads the</span></div>
<div style="position:absolute;left:72.00px;top:542.55px" class="cls_003"><span class="cls_003">value from ADC and determines the number of new cars to be created using the formula below:</span></div>
<div style="position:absolute;left:72.00px;top:590.96px" class="cls_003"><span class="cls_003">pending_cars = 1 + result * (float)5;</span></div>
<div style="position:absolute;left:72.00px;top:634.60px" class="cls_003"><span class="cls_003">Where result is the normalized ADC value and “pending_cars” is the number of vehicles to be</span></div>
<div style="position:absolute;left:72.00px;top:649.15px" class="cls_003"><span class="cls_003">generated.</span></div>
<div style="position:absolute;left:72.00px;top:678.24px" class="cls_003"><span class="cls_003">The value of “pending_cars” is sent to the “XQueue_generate” queue and then this task</span></div>
<div style="position:absolute;left:72.00px;top:692.79px" class="cls_003"><span class="cls_003">suspends itself for 5000 ticks.</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:5614px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background08.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:99.80px" class="cls_004"><span class="cls_004">Task: traffic_state</span></div>
<div style="position:absolute;left:72.00px;top:119.73px" class="cls_003"><span class="cls_003">The “traffic_state task” receives the “pending_cars” value from the “xQueue_generate” queue. It</span></div>
<div style="position:absolute;left:72.00px;top:134.28px" class="cls_003"><span class="cls_003">also receives the “current_light”(indicating red,green or amber light currently on) value from the</span></div>
<div style="position:absolute;left:72.00px;top:148.83px" class="cls_003"><span class="cls_003">“XQueue_light_state queue”. Thereafter, it executes one of two branches of code depending on</span></div>
<div style="position:absolute;left:72.00px;top:163.37px" class="cls_003"><span class="cls_003">the current state ( a separate branch for green light and a branch for yellow and red lights).</span></div>
<div style="position:absolute;left:72.00px;top:192.46px" class="cls_003"><span class="cls_003">The positions of the vehicles are saved in an array of 19 integers named “state”. At the very</span></div>
<div style="position:absolute;left:72.00px;top:207.01px" class="cls_003"><span class="cls_003">beginning of the simulation this array is initialized to 0. A supplemental array named “temp” is</span></div>
<div style="position:absolute;left:72.00px;top:221.56px" class="cls_003"><span class="cls_003">used to hold the current state and is used to update “state” array for the next 1000 ticks. After</span></div>
<div style="position:absolute;left:72.00px;top:236.10px" class="cls_003"><span class="cls_003">the “state” array has been updated its value  is sent over the “xQueue_state” queue and then</span></div>
<div style="position:absolute;left:72.00px;top:250.65px" class="cls_003"><span class="cls_003">the task suspends its execution for a time of 1000 ticks.</span></div>
<div style="position:absolute;left:72.00px;top:293.68px" class="cls_004"><span class="cls_004">Task: display</span></div>
<div style="position:absolute;left:72.00px;top:313.61px" class="cls_003"><span class="cls_003">The display task has the lowest priority. This task receives the current state of the vehicles from</span></div>
<div style="position:absolute;left:72.00px;top:328.16px" class="cls_003"><span class="cls_003">the “xQueue_state” queue. It then calls the “display_led” function which is a middleware</span></div>
<div style="position:absolute;left:72.00px;top:342.70px" class="cls_003"><span class="cls_003">interacting directly with the shift register to display the current state of the simulation by turning</span></div>
<div style="position:absolute;left:72.00px;top:357.25px" class="cls_003"><span class="cls_003">on and off the appropriate LED’s simulating vehicle moment every 1000 ticks.</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:6416px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background09.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.13px" class="cls_002"><span class="cls_002">Algorithms</span></div>
<div style="position:absolute;left:72.00px;top:103.77px" class="cls_004"><span class="cls_004">Algorithm: Traffic generating algorithm</span></div>
<div style="position:absolute;left:72.00px;top:459.43px" class="cls_003"><span class="cls_003">Figure 5 - A flow chart showing the algorithm for traffic generation</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:7218px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background10.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.26px" class="cls_004"><span class="cls_004">Algorithm: System display algorithm</span></div>
<div style="position:absolute;left:72.00px;top:424.66px" class="cls_003"><span class="cls_003">Figure 6 - System display algorithm flow chart</span></div>
<div style="position:absolute;left:72.00px;top:489.54px" class="cls_002"><span class="cls_002">Limitations and Possible Improvements</span></div>
<div style="position:absolute;left:72.00px;top:512.24px" class="cls_003"><span class="cls_003">The solution could be improved in many ways. Firstly a separate branch can be created for the</span></div>
<div style="position:absolute;left:72.00px;top:526.78px" class="cls_003"><span class="cls_003">yellow light state in the “traffic_state” task to improve its readability. It is also possible to</span></div>
<div style="position:absolute;left:72.00px;top:541.33px" class="cls_003"><span class="cls_003">implement the “display” task inside the “traffic_state” task by calling the “display_led”</span></div>
<div style="position:absolute;left:72.00px;top:555.88px" class="cls_003"><span class="cls_003">middleware function directly from the “traffic_state” task. This would have the improvement of</span></div>
<div style="position:absolute;left:72.00px;top:570.42px" class="cls_003"><span class="cls_003">requiring one less queue and one less task thus improving the overall efficiency and</span></div>
<div style="position:absolute;left:72.00px;top:584.97px" class="cls_003"><span class="cls_003">responsiveness of the system.</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:8020px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background11.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.13px" class="cls_002"><span class="cls_002">Summary</span></div>
<div style="position:absolute;left:72.00px;top:93.83px" class="cls_003"><span class="cls_003">The requirements for the Traffic Light System simulation were implemented using 3 queues and</span></div>
<div style="position:absolute;left:72.00px;top:108.38px" class="cls_003"><span class="cls_003">4 tasks. The queues were used for inter-task communication to maintain which traffic light is on,</span></div>
<div style="position:absolute;left:72.00px;top:122.92px" class="cls_003"><span class="cls_003">the number of new vehicles and the state of the vehicles currently in the simulation. The 4 tasks</span></div>
<div style="position:absolute;left:72.00px;top:137.47px" class="cls_003"><span class="cls_003">were used to control which light would be on, generation of vehicles, maintaining and updating</span></div>
<div style="position:absolute;left:72.00px;top:152.02px" class="cls_003"><span class="cls_003">the state of the vehicles on the board and displaying all of the simulation information. System</span></div>
<div style="position:absolute;left:72.00px;top:166.56px" class="cls_003"><span class="cls_003">efficiency could be improved by combining some tasks and removing some queues as</span></div>
<div style="position:absolute;left:72.00px;top:181.11px" class="cls_003"><span class="cls_003">discussed in the previous section.</span></div>
</div>
<div style="position:absolute;left:50%;margin-left:-306px;top:8822px;width:612px;height:792px;border-style:outset;overflow:hidden">
<div style="position:absolute;left:0px;top:0px">
<img src="7d6434da-db64-11eb-a980-0cc47a792c0a_id_7d6434da-db64-11eb-a980-0cc47a792c0a_files/background12.jpg" width=612 height=792></div>
<div style="position:absolute;left:72.00px;top:71.13px" class="cls_002"><span class="cls_002">Sources</span></div>
<div style="position:absolute;left:72.00px;top:108.38px" class="cls_003"><span class="cls_003">[1] ECE 455 Lab Manual</span></div>
<div style="position:absolute;left:72.00px;top:122.92px" class="cls_003"><span class="cls_003">[2]</span><A HREF="https://electronics.stackexchange.com/questions/28091/push-pull-open-drain-pull-up-pull-dow/">https://electronics.stackexchange.com/questions/28091/push-pull-open-drain-pull-up-pull-dow</A> </div>
<div style="position:absolute;left:72.00px;top:137.47px" class="cls_003"><span class="cls_003">n</span></div>
</div>

</body>
</html>
