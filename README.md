# VLSI-LAB-EXPERIMENTS
AIM: To simulate and synthesis Logic Gates,Adders and Subtractor using Xilinx ISE.

APPARATUS REQUIRED: Xilinx 14.7 Spartan6 FPGA

PROCEDURE: STEP:1 Start the Xilinx navigator, Select and Name the New project. STEP:2 Select the device family, device, package and speed. STEP:3 Select new source in the New Project and select Verilog Module as the Source type. STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it. STEP:5 Select the Behavioral Simulation in the Source Window and click the check syntax. STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table. STEP:7 Select the Implementation in the Sources Window and select the required file in the Processes Window. STEP:8 Select Check Syntax from the Synthesize XST Process. Double Click in the Floorplan Area/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained. STEP:9 In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu. STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here. STEP:12 Load the Bit file into the SPARTAN 6 FPGA STEP:11 On the board, by giving required input, the LEDs starts to glow light, indicating the output.

Logic Diagram :

Logic Gates:
![image](https://github.com/navaneethans/VLSI-LAB-EXPERIMENTS/assets/6987778/ee17970c-3ac9-4603-881b-88e2825f41a4)


Half Adder:

![image](https://github.com/navaneethans/VLSI-LAB-EXPERIMENTS/assets/6987778/0e1ecb96-0c25-4556-832b-aeeedfdfe7b9)


Full adder:

![image](https://github.com/navaneethans/VLSI-LAB-EXPERIMENTS/assets/6987778/9bb3964c-438f-469d-a3de-c1cca6f323fb)


Half Subtractor:

![image](https://github.com/navaneethans/VLSI-LAB-EXPERIMENTS/assets/6987778/731470b7-eb4e-49f8-8bb7-2994052a7184)



Full Subtractor:

![image](https://github.com/navaneethans/VLSI-LAB-EXPERIMENTS/assets/6987778/d66f874b-c1f2-44b3-a035-7149b56430c1)



8 Bit Ripple Carry Adder

![image](https://github.com/navaneethans/VLSI-LAB-EXPERIMENTS/assets/6987778/7385a408-40a5-4203-8050-b72818622d79)



VERILOG CODE:
Logic gates:
verilog code
~~~
module logicgates(a,b,andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate);
input a,b;
output andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate;
and(andgate,a,b);
or(orgate,a,b);
xor(xorgate,a,b);
nand(nandgate,a,b);  
nor(norgate,a,b);
xnor(xnorgate,a,b);
not(notgate,a);
endmodule
~~~

OUTPUT:
![WhatsApp Image 2024-04-02 at 6 23 56 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/2e72f13a-5668-4b72-9256-c60baa3df009)
![WhatsApp Image 2024-04-02 at 6 23 52 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/963e0fae-826c-4ee6-93aa-6f6dbdd97ba1)


Half adder:
verilog code:
~~~

module half_add(s,c,a,b);
input a,b;
output s,c;
or (s,a,b);
and (c,a,b);
endmodule
~~~
OUTPUT:
![WhatsApp Image 2024-04-02 at 6 23 49 PM (1)](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/91c95f40-4006-49ef-92ca-6229fdde7afe)
![WhatsApp Image 2024-04-02 at 6 23 49 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/b9553a07-05af-42fd-ad87-e962b4702c28)


Full adder:
verilog code:
~~~
module full_add(sum,cout,a,b,c);
input a,b,c;
output sum,cout;
  assign sum =(a^b^c);
  assign cout=(a&b) | (b&c)| (a&c);

endmodule
~~~

OUTPUT:
![WhatsApp Image 2024-04-02 at 6 23 48 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/182f8bb1-2291-4859-9fbe-3e0969884f97)
![WhatsApp Image 2024-04-02 at 6 23 52 PM (1)](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/777c4867-914c-4ddc-9ae2-8fc0ddd3bc0c)

Half subtractor:
verilog code:
~~~







RESULT:

