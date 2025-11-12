# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER
## NAME: M.V.Vamsidhar Reddy
## REG NO:212224040205
## DATE: 12-11-2025
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

1. Understand: In a SISO shift register, data enters serially and shifts out serially bit by bit.

2. Define module with inputs clk, sin and output q[3:0].

3. Use always block triggered on posedge clk.

4. Shift data: Move each bit right — q[0] <= sin; q[1] <= q[0]; q[2] <= q[1]; q[3] <= q[2];.

5. Apply input: Give serial input bits one by one with each clock pulse.

6. Simulate: Observe bits shifting through the register on every clock edge.

7. Verify: Check that the serial output appears from the last bit q[3].

**PROGRAM**

    /* Program for flipflops and verify its truth table in quartus using Verilog programming.

    module siso(clk, sin, q);
    input clk;
    input sin;
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

    */

**RTL LOGIC FOR SISO Shift Register**

<img width="1907" height="1138" alt="RTL" src="https://github.com/user-attachments/assets/6e461a87-ac89-4967-befd-ae0beab30a80" />


**TIMING DIGRAMS FOR SISO Shift Register**

<img width="1902" height="1113" alt="TIMING DIAGRAM" src="https://github.com/user-attachments/assets/6b43d82a-920a-49ef-a566-01a951ba3c72" />


**RESULTS**

The given SERIES IN SERIES OUT Shift Register is successfully implemented using Verilog HDL in the Quartus Prime.
