# cs220-assignment-8-solved
**TO GET THIS SOLUTION VISIT:** [CS220 Assignment #8 Solved](https://www.ankitcodinghub.com/product/cs220-assignment-8-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;98079&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS220 Assignment #8 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
CS220: Assignment#8

In this assignment, you will design a MIPS processor that can run two given test programs. In other words, you will only implement a subset of the instructions that are sufficient for running the two test programs. I have divided the assignment into two parts for your convenience. The first part focuses on one test program and the second part tests your processor on the second test program.

1. Implement an instruction memory that has width 32 bits and has 14 rows. Initialize the contents of the memory using the following MIPS instruction sequence translated from the C statements shown alongside. All numerical values are represented in decimal in the following program. Each row of memory will store the binary encoding of one MIPS instruction. Use an initial block to store the instructions in instruction memory. Note that the MIPS translation grossly violates the MIPS function calling convention in this problem, but the translation will generate correct result.

<pre>C statements                 MIPS translation
----------------------------------------------------------------------------------
int array[10];
int n, x;
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>int Sum (int n)
{
</pre>
<pre>   // n is in $1
   int i, sum;
   // sum is in $2
   // i is in $3
   sum = 0;
</pre>
<pre>   for (i=0; i&lt;n; i++) {
      if (i == 10) break;        slt   $4, $3, $1
      sum += array[i];           beq   $4, $0, exit // opcode: 0x4, encode exit as 8
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
}

return sum; }

<pre>n = 8;
x = Sum (n);
</pre>
</div>
<div class="column">
<pre>       addiu $5, $0, 10
loop:  beq   $3, $5, exit // encode exit as 6
</pre>
<pre>       lw    $6, 0($3)    // opcode: 0x23
       addu  $2, $2, $6   // opcode: 0x0, func: 0x21
       addiu $3, $3, 1
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>Sum: addiu $2, $0, 0
     addiu $3, $0, 0
</pre>
</div>
<div class="column">
<pre>// opcode: 0x9
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
slt

</div>
<div class="column">
$4, $3, $1

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>// opcode: 0x0, func: 0x2a
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>$4, $0, loop // opcode: 0x5, encode loop as -5
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>       bne
exit:  jr    $31          // opcode: 0x0, func: 0x8, rs: 31
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>lw    $1, 10($0)
jal   Sum          // opcode: 0x3, encode Sum as 0
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
Implement a data memory of width eight bits and having 11 rows for storing array[10] in the first ten rows and n in the last row. Use an initial block for storing these in eight-bit two’s complement representation in the data memory. We will design a simple MIPS processor that implements all instructions shown in this program (addiu, slt, beq, lw, addu, bne, jr, jal) and ignores all overflows. The “word” for this processor is eight bits long. The processor will have a register file having 32 registers each of width eight bits. Initialize all registers to zero. In all I-format instructions, the least significant eight bits of the 16-bit immediate operand will be used in the actual

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
operation. Initialize an eight-bit program counter register to 12 (address of the instruction corresponding to n = 8). In beq and bne, the program counter of the branch target should be computed by adding the least significant eight bits of the offset to the program counter of the branch instruction. In lw, the computed address should be treated as the row number of data memory. In jal, the address of the call target is same as the least significant eight bits of the target field of the instruction. The MIPS processor is implemented as a seven-state FSM as outlined below. Initially, the state is zero. Each state’s operations are done on posedge of clock.

<ul>
<li>State 0: reads the instruction from the instruction memory row pointed to by the program counter and sets state to 1.</li>
<li>State 1: finds out the fields of the instruction and sets state to 2.</li>
<li>State 2: reads the source register operands of the instruction from the register file and sets state to 3.</li>
<li>State 3: executes the instruction if the instruction is addiu, addu, slt, beq, bne, jal, or jr; if the instruction is lw, its address is computed; otherwise marks the instruction as invalid. Sets the program counter of the next instruction appropriately. Sets state to 4.</li>
<li>State 4: accesses data memory if the instruction is lw and reads the row pointed to by the address computed in the last state; other instructions do nothing in this state. Sets state to 5.</li>
<li>State 5: if the instruction is not marked invalid and produces a result in a destination register and the destination register is not $0, writes the result of the instruction to the destination register. Sets state to 0 if program counter is less than ‘MAX PC; otherwise sets state to 6. MAX PC should be defined as 14.</li>
<li>State 6: outputs the contents of register ‘OUTPUT REG and a done signal. It stays in state 6. OUTPUT REG should be defined as 2 for this program because $2 will have the value of x, which is of interest to us.
Your design should work for arbitrary initial values of array elements and n. While implementing the slt instruc- tion, the comparison operands should be treated signed. Therefore, instead of writing “a &lt; b”, your Verilog code should say “$signed(a) &lt; $signed(b)” where $signed is an in-built Verilog function to convert unsigned variables (default for all variables in Verilog) to signed.

To help grading, clearly mark the place where you initialize your data memory.

Note to TAs for grading: Please test the implementation by initializing the array and n. Note that even if you set n to be more than 10, only ten elements of the array will be considered in the computation. Please have a few of the array elements as negative (you can go up to -128 on the negative side and 127 on the positive side). Also, note that the sum must be in the range -128 to 127. So, choose your data memory contents accordingly to avoid overflow.

2. [10 marks] Implement an instruction memory that has width 32 bits and has 11 rows. Initialize the contents of the memory using the following MIPS instruction sequence translated from the C statements shown alongside. All numerical values are represented in decimal in the following program. Each row of memory will store the binary encoding of one MIPS instruction. Use an initial block to store the instructions in instruction memory.

<pre>C statements                 MIPS translation
----------------------------------------------------------------------------------
int a, b, c, i, sum;
a = -20;
b = 10;
c = 2;
sum = 0;
</pre>
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>lw    $1, 0($0)
lw    $2, 1($0)
lw    $3, 2($0)
addiu $4, $0, 0
</pre>
</div>
<div class="column">
<pre>// opcode: 0x23
</pre>
<pre>// opcode: 0x9
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
<pre>for (i=a; i&lt;b; i+=c) {
   sum += i;
</pre>
}

</div>
<div class="column">
<pre>addiu $5, $1, 0
slt   $6, $5, $2    // opcode: 0x0, func: 0x2a
beq   $6, $0, exit  // opcode: 0x4, encode exit as 5
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>                      loop:  addu  $4, $4, $5    // opcode: 0x0, func: 0x21
                             addu  $5, $5, $3
</pre>
<pre>                             slt   $6, $5, $2
                             bne   $6, $0, loop  // opcode: 0x5, encode loop as -3
</pre>
exit:

Implement a data memory of width eight bits and having three rows for storing a, b, c. Use an initial block for storing a, b, c in eight-bit two’s complement representation in the data memory. The MIPS processor designed in the first part already implements all the necessary instructions needed to run this program. So, you can just copy your processor modules and change the contents of the instruction and data memories. The other changes are: (i) MAX PC should be defined as 11 and (ii) OUTPUT REG should be defined as 4 for this program because $4 will have the value of sum, which is of interest to us. Your design should work for arbitrary initial values of a, b, c. To help grading, clearly mark the place where you initialize these variables in your data memory.

Note to TAs for grading: Please test the implementation by initializing a, b, c. Please have a few of the numbers as negative (you can go up to -128 on the negative side and 127 on the positive side). Also, note that the sum must be in the range -128 to 127. So, choose your data memory contents accordingly to avoid overflow.

</div>
</div>
</div>
