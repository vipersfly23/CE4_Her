CE4_Her
=======

Computer Exercise 4.


###Program A

![alt text](https://github.com/vipersfly23/CE2/blob/master/Behavorial_Simulation.GIF?raw=true "Program A")


#####Simple Memory Manipulation: 

Write a program that stores the value $9 in location $B0, $8 in $C4 and $B in $CB. (Target program end: $11)

Step 1) The program calls the instruction: LDAI , and loads 9 into the accumulator

Step 2) The program calls the instruction STA, and stores the value 9 into the RAM labeled One

Step 3) The program calls the instruction: LDAI , and loads 8 into the accumulator

Step 4) The program calls the instruction STA, and stores the value 8 into the RAM labeled Two

Step 5) The program calls the instruction: LDAI , and loads B into the accumulator

Step 6) The program calls the instruction STA, and stores the value B into the RAM labeled Three


#####Mathematics: 

Write a program that retrieves a value from location $B0, doubles it, and subtracts 4.  The result should be output to Port 2. You will need to place a positive test value in this location prior to running the program.  Although RAM is volatile and you normally cannot directly change values in it without having a program do it, you can in this simulation by checking “Allowed RAM values to be edited” in the Programming Wizard.  (Target program end: $0C)

Step 1) The program calls the instruction LDAD, which loads a value from the RAM labeled one.

Step 2) The program calls the instruction ADDD, which adds the value from RAM labeled one to the accumulator

(Ultimately doubling the value in the accumulator)

Step 3) The program calls the instruction STA, which stores the value in the accumulator to the RAM labeled Two

Step 4) The program calls the instruction LDAI, which loads the 4 into the accumulator.

Step 5) The program calls the instruction NEG, which takes the twos complement of the number.

Step 6) The program calls the instruction ADDD, which adds the value stored in RAM labeled two to the accumulator

Step 7) The program calls the instruction OUT, which outputs the value in the accumulator to output port 2.

#####Loops: 

Write a program that starts by reading what is on Input Port 3 and then displaying that on Output Port 0.  One less than that should then display on Port 1 and one less than what is on Port 1 will display on Port 2.  The program then decrements what is on Port 0, then decrements what is on Port 1, then decrements what is on Port 2.  This process is continued in an infinite loop (i.e. If Input Port 3 contains a ‘2’ , Ports 0-2 will show 2,1,0, respectively.  The 2, 1, 0 will then change to 1,0,F, then 0, F, E, and so on). (Target program end: $10)

Step 1) The program calls the instruction LDAI, which loads the value 1 into the accumulator.

Step 2) The program calls the instruction NEG, which takes the two's complement of the number

Step 3) The program calls the instruction STA, which stores the value in the accumulator to the RAM labeled Two

Step 4) The program calls the instruction IN, which takes in a value from the input port 3,

Step 5) The program calls the instruction OUT, which outputs the value in the accumulator to output port 0

Step 6) The program calls the instruction ADDD, which adds the value from the RAM labeled two to the accumulator

Step 7) The program calls the instruction OUT, which outputs the value in the accumulator to output port 1

Step 8) The program calls the instruction ADDD, which adds the value from the RAM labeled two to the accumulator

Step 9) The program calls the instruction OUT, which outputs the value in the accumulator to output port 2

Step 10) The program calls the instruction ADDD, which adds the value from the RAM labeled two to the accumulator

Step 11) The program calls the instruction JMP, which jumps to the label loop. Program returns to step 5 and repeats.




