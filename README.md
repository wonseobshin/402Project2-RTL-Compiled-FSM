RTL Compiled SkyTrain Gate
====================
402 Project 2 Report
--------------------

By Won Seob Shin, 49820153

About
-----
As an extension of [Project 1](https://github.com/wonseobshin/402Project1-Simple-SkyTrain-Gate-FSM), we now simulate the FSM at Register Transfer Level (RTL) using Cadence.


Mapped Verilog from the RTL Compiler
---------------------------
![FSM-mapped](https://github.com/wonseobshin/402Project1-Simple-SkyTrain-Gate-FSM/blob/master/fsm.jpg)

Waves
-----------------

When simulated on ModelSim, we get the following waves.

![New Wave](https://github.com/wonseobshin/402Project1-Simple-SkyTrain-Gate-FSM/blob/master/DUT_diagram.jpg)

![New Wave2](https://github.com/wonseobshin/402Project1-Simple-SkyTrain-Gate-FSM/blob/master/DUT_diagram.jpg)

When compared to the previously generated (non-mapped) simulation, we can see that the waves are identical.

![Old Wave](https://github.com/wonseobshin/402Project1-Simple-SkyTrain-Gate-FSM/blob/master/DUT_diagram.jpg)

Cell Count
-------------

The RTL compiler generates reports in the [output_files folder](https://github.com/wonseobshin/402Project2-RTL-Compiled-FSM/tree/master/output_files), where we can find how many cells were used in the design.

![Power Report](https://github.com/wonseobshin/402Project1-Simple-SkyTrain-Gate-FSM/blob/master/70769078_2362328880762682_2160517525123629056_n.jpg)

Changes made post-project 1
----
Some changes were made to increase the number of cells used in the design to follow the requirements set by the project description.
    
    - Added the funtionality to make (output) an error sound
    - Display accurate and descriptive error on screen by adding states
    - Removed unecessary latches
    *But no major changes were made*

Challenges
------

Although running the script (RTLCompiler.tcl --- added to gitignore to protect personal data) was fairly straight forward, various changes had to be made to make it work without errors on my machine.

Latches were also a big problem towards the end, as I did not realize there were latches. In the future, I will keep close attention to what kind of latches I create by covering all cases, adding default statements, and having a reset in all machine designs.