# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**
1.Open Intel Quartus Prime and create a new Verilog HDL project.

2.Create a new Verilog file and write the program for the JK Flip-Flop using if-else statements.

3.Save the file with .v extension and compile the design to check for syntax errors.

4.Create the required input signals (J, K, Clock, Reset) using the waveform editor or testbench.

5.Run the simulation and observe the outputs Q and Q̅ (QB) for different input combinations.

6.Verify the obtained outputs with the JK Flip-Flop functional/truth table.

7.Record the simulation results and conclude that the JK Flip-Flop operation is verified successfully.

**PROGRAM**
Developed By; Jijo H Jebas Register Number: 212225040156
```
module Exp7(q, qb,j,k,clock,reset);
input j,k,clock,reset;
output reg q, qb;
always @ (posedge (clock))
    begin 
        if (!reset)
            begin
               q <= q;
               qb <=qb;
            end  
else
            begin
               if (j == 0 && k == 0)
                    begin
                    q <= q;
qb <= qb;
                    end 
else if (j != k)
                    begin
                    q <= j;
                    qb <= k;
                    end
               else if (j == 1 && k == 1) 
                    begin 
                    q <= ~q; 
                    qb <= ~qb; 
                    end 
            end
end  
endmodule
```

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL LOGIC FOR FLIPFLOPS**
<img width="982" height="598" alt="{DE7E47E1-2BA8-45A7-B94F-0E7944F7641F}" src="https://github.com/user-attachments/assets/d351bb65-a055-4744-98f4-164be3aac2db" />

**TIMING DIGRAMS FOR FLIP FLOPS**
<img width="1920" height="1080" alt="{B31D32BB-7C5E-4B43-9763-8D437969AF53}" src="https://github.com/user-attachments/assets/a1192da9-44f8-4bea-ab30-ec9b69e99963" />

**RESULTS**
Thus we go the output...
