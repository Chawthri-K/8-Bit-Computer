# 8-Bit-Computer
Foreward: The inspiration for this design is a Youtuber by the name of Ben Eater. He has a lot of information and documentation regarding 8-bit computers.

The goal:
To make a computer, entirely from basic IC's (primarily the 7400 series). The design for the CPU is heavily influenced by Ben Eater, who designed an 8-bit computer on breadboards. 
The main difference between my design, is that I wanted to put everything on PCB
a) For more reliable connections 
b) So it'd look cooler

Instead of designing everything on one board, I'm opting for a more modular design, where major sub-systems would be on a single PCB and those sub-systems would be connected together via a wire harness. Almost like a modern day laptop, except it's just the CPU being spread out on multiple PCB's. The biggest advantage to this, apart from modularity and upgradability is the cost. You can purchase 10 copies of any PCB with dimensions under 100 x 100 mm for just $2. The current design only has 6 subsystems plus two boards for a bus, this means I can get the PCB for under $20 (+shipping)... and I'll get 10 copies. This option is much cheaper than designing the entire thing on one board and getting the entire thing printed. Furthermore, if a single sub-system fails, I can just replace that bit, instead of having to do a board repair on the entire thing.

Current Progress:

There's four main stages to this project:
Research and planning
Design
Testing and Building
Troubleshooting

I am currently at the design stage.

The two most time consuming parts to this (for me) are the research and planning stage and the trouble shooting stage. At my current level of experience, while there will definitely be some challenges presented from actually designing the circuit boards and putting them together, I am familiar enough with surface mount soldering and Altium Designer, that these two stages won't take too long.

Getting familiar with all the various subsystems, and learning about how things like RAM, Arithmetic Logic Units, Registers, etc. work took a large amount of time. At this point I've already designed, built and succesfully tested the clock circuit.

![1](https://lh3.googleusercontent.com/FS6w4m2e8pii9Z1oz3WwmEprHnBDDs-JRLz8bvKE7lH6wFhR4spKnxLRgqs37KZ2QtcpMm8LDjScWT-GkDyGG7sWnDWx-o2P20GCP6_v39tsnVzx_WQ-rqy6BIXuJUZDtjTTnwjpyvzsxtSGTOr9DjDNaBGei_1If7PsFrl1Tv4fnlLCTZl6q4UGOMFwmDbxOdafRrSQGMn-HWP6lK6kmKTGEo-XTSLPSFfiwTdWq1Z0rdchfzuu9Iz78ChcPp0EC6mgtNEH34m5IVbDrACr4vzRUkGDR7ar6xQnHB2XHmgIum4OiSYbgcjsqbYFlJ_WkmHrfV8w0XNRtKsvErndYjeg8rGkEHqTtqPtZYJcc-0kp6O-2WgS79084RDPmUXvX5rAuif943Dhny9bDaUcWlIv5t9POWfr2R9C5h2-VLkwSxx8d2agdRw8qaQoSNMoYDOswXxLn6nWuK_vdFXBNo0v2DdWHeA2XJg-nmDxTcCpxgc-DIL_17D5vfoa5lixO2NokmBxTWwgiuzRXvsAS27DGm4fdQ07fdwVOk7gP4KjgthVui2nEN7Gc5JN4wDIuwq3BDSw6rv4o73qdZJyHJsgCcATur3AJtyffMRriMBa-YTeFNT3J4DK6dtM0NGn=w870-h775-no)

My expected time to complete design is around the start of October, depending on how busy I get with school.

From there I'll have to wait a couple weeks for parts and the boards to arrive, before I can begin assembly.

Ideally, the entire computer will work on it's first try... but since this is electronics, it will almost definitely not, so I'll need to spend a fair bit of time after building, fixing up all the bugs.

The major subsystems in the project are:

The Clock:
This keeps track of time using a 555 timer in an astable multivibrator configuration. It also, incorporates a bistable and monostable multivibrator circuit, which allows it to toggle between regular operations and manually stepping the clock.

The Registers:
While it doesn't contain all the registers, it will contain all major ones including the A and B register, the ALU and a 4-bit FLAGS register.

The Memory:
This is just the RAM as well as the memory address register, which calls on various locations in memory.

The Program Counter:
This is the smallest sub-system, it does as the name implies, keeps track of which step the program is on.

The Output:
This is just some 7-segment displays, along with an EEPROM so replace combinational logic to show the value calculated by the computer.

The Controls:
THis includes the acutal control logic (again an EEPROM, in place of combinational logic), which will connect all over the CPU to transmit instructions, as well as the Instruction Register, which provides the instructions to the control logic.

Future Aspirations:
So apart from just building the CPU, in the future I would also like to implement a basic graphics card/display (using RGB LED's, implemented in a format similar to the Commodore 64), a sound card (using the old school style of multiple voices), and a controller (keyboard/mouse). These three other components will require about the same amount of effort to build as the CPU, except I won't have any designs to follow. However, with the knowledge I have learned from building the CPU, I am confident I am able to design these parts.

At the moment I'm just focused on getting the CPU built :) I'll worry about the other parts in the future. I'll most likely create seperate repos for them.
