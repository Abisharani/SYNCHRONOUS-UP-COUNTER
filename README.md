### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram
**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:ABISHA RANI S
RegisterNumber:24900748
*/
...
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule

 module ex12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule
...
**RTL LOGIC UP COUNTER**
![Screenshot (38)](https://github.com/user-attachments/assets/db69df4e-b724-4161-a4a2-b2921654e4cd)
![Screenshot (40)](https://github.com/user-attachments/assets/eaa84a83-b922-46da-819b-2452679af6e5)

**TIMING DIAGRAM FOR IP COUNTER**
![Screenshot (39)](https://github.com/user-attachments/assets/fdbec389-f1cd-4c17-9769-ecd8d477bfef)
![Screenshot (41)](https://github.com/user-attachments/assets/19fdf48e-4995-40ce-8446-d4cce0f0de8a)

**TRUTH TABLE**
![Screenshot 2024-12-11 183102](https://github.com/user-attachments/assets/52725080-0080-4828-9b9e-4749d6ba10be)
![Screenshot 2024-12-11 183130](https://github.com/user-attachments/assets/5868f9fb-4986-4dfa-a2b1-2d93fe79f0ec)

**RESULTS**
To implement 4 bit synchronous up counter and validate functionality is verified.
