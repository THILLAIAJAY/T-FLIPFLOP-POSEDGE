# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

/* write all the steps invloved */
1.Open quartus II and create New project wizard. 2. Write the program in Verilog HDL file and run the program. 3. Download the RTL viewer 4. Now open university program VWF and download
waveform after the execution.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
```
module exp_6(T,clk,Q,Qbar);
input T,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk) begin Q=(T&(~Q))|((~T)&Q);
Qbar=~Q;
end endmodule
```
Developed by:THILLAIAJAY L
RegisterNumber:24008308
*/

**RTL LOGIC FOR FLIPFLOPS**

![exp 9](https://github.com/user-attachments/assets/e79e687a-7d15-4ef3-bf21-1f2aeed49e41)

**TIMING DIGRAMS FOR FLIP FLOPS**

![exp 09](https://github.com/user-attachments/assets/59108102-d884-4777-a922-7680512deee6)

**RESULTS**

Thus the Flip flop designed and the truth tables is verified using Quartus software.
