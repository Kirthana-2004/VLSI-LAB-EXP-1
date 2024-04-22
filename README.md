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

module half_subtractor(d,b0,a,b);
input a,b;
output d,b0;
assign d = a^b;
assign b0 = (~a)&b;
endmodule
~~~

OUTPUT:
![WhatsApp Image 2024-04-02 at 6 23 48 PM (1)](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/0f992b52-92dd-4626-9e01-a50d12e6f778)
![WhatsApp Image 2024-04-02 at 6 23 53 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/062966a5-d357-4b78-bf28-1308f37322cd)

Full subtractor:
verilog code:
~~~
module full_subtractor(a,b,c,d,bout);
input a,b,c;
output d,bout;
assign d = a^b^c;
assign bout = (~a&b) | (~(a^b)&c);
endmodule
~~~

OUTPUT:
![WhatsApp Image 2024-04-22 at 2 31 18 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/e65684f5-b464-4ba9-ba16-6015b3620a1c)
![WhatsApp Image 2024-04-02 at 6 23 53 PM (1)](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/d799e4b7-6f10-4b1a-bb0d-d6119ea85f28)


4 Bit Ripple Carry Adder:
verilog code:
~~~
module rippe_adder(S, Cout, X, Y,Cin);
 input [3:0] X, Y;
 input Cin;
 output [3:0] S;
 output Cout;
 wire w1, w2, w3;
 fulladder u1(S[0], w1,X[0], Y[0], Cin);
 fulladder u2(S[1], w2,X[1], Y[1], w1);
 fulladder u3(S[2], w3,X[2], Y[2], w2);
 fulladder u4(S[3], Cout,X[3], Y[3], w3);
endmodule
module fulladder(S, Co, X, Y, Ci);
  input X, Y, Ci;
  output S, Co;
  wire w1,w2,w3;
  xor G1(w1, X, Y);
  xor G2(S, w1, Ci);
  and G3(w2, w1, Ci);
  and G4(w3, X, Y);
  or G5(Co, w2, w3);
endmodule
~~~

OUTPUT:
![WhatsApp Image 2024-04-22 at 2 24 44 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/e54ef17e-86e0-41ab-991d-e6211ad9c5a1)
![WhatsApp Image 2024-04-22 at 2 24 38 PM](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/9d4125ba-6e1f-42e5-9888-bf79bff0e44e)


8 Bit Ripple Carry Adder:
verilog code:
~~~
module ripplemod(a, b, cin, sum, cout);
input [07:0] a;
input [07:0] b;
input cin;
output [7:0]sum;
output cout;
wire[6:0] c;
fulladd a1(a[0],b[0],cin,sum[0],c[0]);
fulladd a2(a[1],b[1],c[0],sum[1],c[1]);
fulladd a3(a[2],b[2],c[1],sum[2],c[2]);
fulladd a4(a[3],b[3],c[2],sum[3],c[3]);
fulladd a5(a[4],b[4],c[3],sum[4],c[4]);
fulladd a6(a[5],b[5],c[4],sum[5],c[5]);
fulladd a7(a[6],b[6],c[5],sum[6],c[6]);
fulladd a8(a[7],b[7],c[6],sum[7],cout);
endmodule
module fulladd(a, b, cin, sum, cout);
input a;
input b;
input cin;
output sum;
output cout;
assign sum=(a^b^cin);
assign cout=((a&b)|(b&cin)|(a&cin));
endmodule
~~~

OUTPUT:
![WhatsApp Image 2024-04-22 at 2 24 37 PM (1)](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/ff3873d7-ae9c-4829-af92-a11e5215fc56)
![WhatsApp Image 2024-04-22 at 2 24 38 PM (1)](https://github.com/Kirthana-2004/VLSI-LAB-EXP-1/assets/144320880/ba1027cc-3d2b-473e-aebe-291e24ddd6cb)



RESULT:
Hence the simulation and synthesis of full adder,full subtractor,half adder,half subtractor,logic gates,ripplecarryadder_4bit,ripplecarryadder_8bit using vivado 2023.2. was successfully simulated using vivado.2023.3.








RESULT:

