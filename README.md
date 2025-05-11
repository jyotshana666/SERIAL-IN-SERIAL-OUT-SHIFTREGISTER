# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

Step 1: Initialize the Shift Register Initialize the shift register with n bits, where n is the number of bits in the shift register. Set all bits to 0.

Step 2: Receive Input Bit Receive a new input bit (I) from the serial input.

Step 3: Shift Bits to the Right Shift the current contents of the shift register one bit to the right.

Step 4: Load Input Bit into MSB Load the new input bit (I) into the most significant bit (MSB) position.

Step 5: Output LSB Output the least significant bit (LSB) of the shift register as the serial output.

Step 6: Repeat Repeat steps 2-5 for each new input bit.

**PROGRAM**
```
module exp10(clk,sin,q);
input clk,sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin 
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end 
endmodule
```
Developed by: JYOTTSHANA S R

RegisterNumber: 212224230111


**RTL LOGIC FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/f980faaa-e193-4811-b350-74f1783fe202)

**TIMING DIGRAMS FOR SISO Shift Register**

![image](https://github.com/user-attachments/assets/d3a30ca6-f9f1-44b5-9ca0-11567fff2272)


**RESULTS**

SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
