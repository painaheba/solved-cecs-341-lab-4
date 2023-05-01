Download Link: https://assignmentchef.com/product/solved-cecs-341-lab-4
<br>
<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Lab 4: MIPS Datapath for R-type Instructions </strong>

<strong> </strong>







<h1>1     Objective</h1>

The objective of this lab is to design a MIPS datapath for R-type instructions (specified in Table 1) as illustrated in Figures 1 to 6.










<h1>2     Required Knowledge</h1>

<ul>

 <li>How to write VHDL code using the behavioral and structural models.</li>

</ul>




Figure 1: Top-level block diagram of Datapath













Dout Dout










Figure 2: Program counter register (PC)                  Figure 3: Program counter adder (PCADD)




Dout Dout

Din Din










Figure 4: Control                                                     Figure 5: ALU control




<ul>

 <li>How to use packages in VHDL.</li>

</ul>




<ul>

 <li>How to use the Xilinx Vivado Design Suite to write VHDL code, create block designs, add VHDL modules to block designs and create test benches.</li>

</ul>







<h1>3     Design</h1>

The objective of this lab is to design the MIPS datapath (and control unit) to implement the R-type instructions listed in Table 1. To accomplish this, the following components must first be designed using behavioral VHDL:




<ul>

 <li>The Program Counter (PC) (Figure 2)</li>

</ul>




<ul>

 <li>The Control Unit (Figure 4)</li>

</ul>




<ul>

 <li>The ALU Control Unit (Figure 5)</li>

</ul>




<ul>

 <li>The PCADD (Figure 3)</li>

</ul>




In addition, a working design for the ALU, Register-File and Instruction Memory are provided on the Beachboard. You will have to <strong>modify </strong>the provided ALU to add the functionality for the <em>slt </em>instruction. The provided Register-File and Instruction memory units <strong><u>must be </u></strong>used as they are pre-loaded with initial values and the test program, respectively.

The datapath should be designed as a block design. Figure 6 illustrates the connections between the components. Table 2 includes all the components that must be designed, as well as the datapath, and the method by which the design is to be implemented.




Figure 6: Datapath for R-type instructions

<h2>Table 1: R-type instructions to implement</h2>

<table width="498">

 <tbody>

  <tr>

   <td width="36">No</td>

   <td width="182">Operation</td>

   <td width="95">Mnemonic</td>

   <td width="90">Opcode<em>hex </em></td>

   <td width="96">Function<em>hex </em></td>

  </tr>

  <tr>

   <td width="36">1</td>

   <td width="182">Add</td>

   <td width="95"><em>add </em></td>

   <td width="90">00</td>

   <td width="96">20</td>

  </tr>

  <tr>

   <td width="36">2</td>

   <td width="182">Add unsigned</td>

   <td width="95"><em>addu </em></td>

   <td width="90">00</td>

   <td width="96">21</td>

  </tr>

  <tr>

   <td width="36">3</td>

   <td width="182">Subract</td>

   <td width="95"><em>sub </em></td>

   <td width="90">00</td>

   <td width="96">22</td>

  </tr>

  <tr>

   <td width="36">4</td>

   <td width="182">Subract unsigned</td>

   <td width="95"><em>subu </em></td>

   <td width="90">00</td>

   <td width="96">23</td>

  </tr>

  <tr>

   <td width="36">5</td>

   <td width="182">And</td>

   <td width="95"><em>and </em></td>

   <td width="90">00</td>

   <td width="96">24</td>

  </tr>

  <tr>

   <td width="36">6</td>

   <td width="182">Or</td>

   <td width="95"><em>or </em></td>

   <td width="90">00</td>

   <td width="96">25</td>

  </tr>

  <tr>

   <td width="36">7</td>

   <td width="182">Xor</td>

   <td width="95"><em>xor </em></td>

   <td width="90">00</td>

   <td width="96">26</td>

  </tr>

  <tr>

   <td width="36">8</td>

   <td width="182">Nor</td>

   <td width="95"><em>nor </em></td>

   <td width="90">00</td>

   <td width="96">27</td>

  </tr>

  <tr>

   <td width="36">9</td>

   <td width="182">Set less than</td>

   <td width="95"><em>slt </em></td>

   <td width="90">00</td>

   <td width="96">2A</td>

  </tr>

  <tr>

   <td width="36">10</td>

   <td width="182">Set less than unsigned</td>

   <td width="95"><em>sltu </em></td>

   <td width="90">00</td>

   <td width="96">2B</td>

  </tr>

 </tbody>

</table>

<sub> </sub>

*<em>For splitting a bus into smaller width buses, use the Slice IP. </em>

*<em>Use the specified names for both file and input and output ports in case of datapath. </em><em> </em>

<h1>4     Testing</h1>

The registers in the register file are initialized to values shown in Table 3. The instruction memory contains the test program which is shown in below. Calculate the final values of the registers after the completion of the execution of the test program and complete Table 3.

<h2>Table 2: Components to design</h2>

<table width="393">

 <tbody>

  <tr>

   <td width="35">No</td>

   <td width="142">Component</td>

   <td width="107">VHDL model</td>

   <td width="108">Design model</td>

  </tr>

  <tr>

   <td width="35">1</td>

   <td width="142">PC</td>

   <td width="107">Behavioral</td>

   <td width="108">HDL</td>

  </tr>

  <tr>

   <td width="35">2</td>

   <td width="142">PCADD</td>

   <td width="107">Behavioral</td>

   <td width="108">HDL</td>

  </tr>

  <tr>

   <td width="35">3</td>

   <td width="142">Control Unit</td>

   <td width="107">Behavioral</td>

   <td width="108">HDL</td>

  </tr>

  <tr>

   <td width="35">4</td>

   <td width="142">ALU Control Unit</td>

   <td width="107">Behavioral</td>

   <td width="108">HDL</td>

  </tr>

  <tr>

   <td width="35">5</td>

   <td width="142">Datapath</td>

   <td width="107">–</td>

   <td width="108">Block Design</td>

  </tr>

 </tbody>

</table>







Build a testbench with a clock period of <em>20ns </em>and run the simulation for 1 clock cycles with reset=’1’ and for 10 clock cycles with reset=’0’. Compare the final values of the registers from the simulation with the values you calculated in Table 3.




<strong>The test program in instruction memory </strong>

<strong> </strong>

<strong> </strong>

add $t0, $t1, $t2 addu $t1, $t2, $t3 and $t2, $t3, $t4 nor $t3, $t4, $t5 or $t4, $t5, $t6 xor $t5, $t6, $t7 sub $s0, $s1, $s2 subu $s1, $s2, $s3 slt $s2, $s3, $s4 sltu $s3, $s4, $s5




<h2>Table 3. Initial values of registers</h2>

<table width="560">

 <tbody>

  <tr>

   <td rowspan="2" width="36">No</td>

   <td rowspan="2" width="73">Register</td>

   <td colspan="2" width="226">Calculated</td>

   <td colspan="2" width="226">Simulated</td>

  </tr>

  <tr>

   <td width="116">Initial value<em>hex </em></td>

   <td width="110">Final value<em>hex </em></td>

   <td width="116">Initial value<em>hex </em></td>

   <td width="110">Final value<em>hex </em></td>

  </tr>

  <tr>

   <td width="36">0</td>

   <td width="73">$zero</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">1</td>

   <td width="73">$at</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">2</td>

   <td width="73">$v0</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">3</td>

   <td width="73">$v1</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

 </tbody>

</table>




<table width="560">

 <tbody>

  <tr>

   <td width="36">4</td>

   <td width="73">$a0</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">5</td>

   <td width="73">$a1</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">6</td>

   <td width="73">$a2</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">7</td>

   <td width="73">$a3</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">8</td>

   <td width="73">$t0</td>

   <td width="116">00000009</td>

   <td width="110"></td>

   <td width="116">00000009</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">9</td>

   <td width="73">$t1</td>

   <td width="116">0000000A</td>

   <td width="110"></td>

   <td width="116">0000000A</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">10</td>

   <td width="73">$t2</td>

   <td width="116">0000000B</td>

   <td width="110"></td>

   <td width="116">0000000B</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">11</td>

   <td width="73">$t3</td>

   <td width="116">0000000C</td>

   <td width="110"></td>

   <td width="116">0000000C</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">12</td>

   <td width="73">$t4</td>

   <td width="116">0000000D</td>

   <td width="110"></td>

   <td width="116">0000000D</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">13</td>

   <td width="73">$t5</td>

   <td width="116">0000000E</td>

   <td width="110"></td>

   <td width="116">0000000E</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">14</td>

   <td width="73">$t6</td>

   <td width="116">0000000F</td>

   <td width="110"></td>

   <td width="116">0000000F</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">15</td>

   <td width="73">$t7</td>

   <td width="116">00000010</td>

   <td width="110"></td>

   <td width="116">00000010</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">16</td>

   <td width="73">$s0</td>

   <td width="116">00000011</td>

   <td width="110"></td>

   <td width="116">00000011</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">17</td>

   <td width="73">$s1</td>

   <td width="116">00000012</td>

   <td width="110"></td>

   <td width="116">00000012</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">18</td>

   <td width="73">$s2</td>

   <td width="116">00000013</td>

   <td width="110"></td>

   <td width="116">00000013</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">19</td>

   <td width="73">$s3</td>

   <td width="116">00000014</td>

   <td width="110"></td>

   <td width="116">00000014</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">20</td>

   <td width="73">$s4</td>

   <td width="116">00000015</td>

   <td width="110">  </td>

   <td width="116">00000015 </td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">21</td>

   <td width="73">$s5</td>

   <td width="116">00000016</td>

   <td width="110"></td>

   <td width="116">00000016</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">22</td>

   <td width="73">$s6</td>

   <td width="116">00000017</td>

   <td width="110"></td>

   <td width="116">00000017</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">23</td>

   <td width="73">$s7</td>

   <td width="116">00000018</td>

   <td width="110"></td>

   <td width="116">00000018</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">24</td>

   <td width="73">$t8</td>

   <td width="116">00000019</td>

   <td width="110"></td>

   <td width="116">00000019</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">25</td>

   <td width="73">$t9</td>

   <td width="116">0000001A</td>

   <td width="110"></td>

   <td width="116">0000001A</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">26</td>

   <td width="73">$k0</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">27</td>

   <td width="73">$k1</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">28</td>

   <td width="73">$gp</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">29</td>

   <td width="73">$sp</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">30</td>

   <td width="73">$fp</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

  <tr>

   <td width="36">31</td>

   <td width="73">$ra</td>

   <td width="116">00000000</td>

   <td width="110"></td>

   <td width="116">00000000</td>

   <td width="110"></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong> </strong>


