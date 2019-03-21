# OS-Power-Supply
Re-implementation of my Power Supply code with task switching.
To overcome issue with slow devices such as SPI, and I2C memory I'm employing 'task switching' to the project. 
Currently each sub-system is grouped into a task with it's own stack and register set. When necessary the task's stack,
and a copy of it's registers (W0-W15, Status Register, and Program Counter) are loaded into the dsPIC33F's memory. 
From that point the process continues where it left off until it's time quantum has expired, or it completes. Some 
tasks by design will never complete. Other tasks will run to completion due to there short size. Still other tasks 
are one shot tasks which may or maynot exhaust there quantum.

# More to come 
