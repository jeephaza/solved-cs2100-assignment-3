Download Link: https://assignmentchef.com/product/solved-cs2100-assignment-3
<br>
<h1>Question 0.</h1>

<ul>

 <li>You have named your file with your student number, i.e., <strong>pdf</strong>.</li>

 <li>You have submitted your assignment as a <strong>single PDF file</strong> and no multiple copies.</li>

 <li>Your assignment submission has your <strong>tutorial group number</strong>, <strong>student number</strong> and <strong>name</strong> at the top of the first page of your file. (All three items must be present.)</li>

</ul>

<strong>Question 1. MSI Devices  </strong>

Note:

&#x25aa; Boolean constants (0 and 1) are always available; &#x25aa; Complemented literals are <u>not</u> available.

<ul>

 <li>Given the following circuit showing a 4:1 multiplexer and an AND gate, what is the simplified</li>

</ul>

SOP expression of the function <em>F</em>(<em>A</em>,<em>B</em>,<em>C</em>,<em>D</em>)?




<ul>

 <li>Implement the following Boolean function using a single 4:1 multiplexer without any logic gate. Once you have chosen the 2 variables for the selector lines, those 2 variables are <u>not</u> to appear in the 4 multiplexer inputs.</li>

</ul>

No mark will be awarded if any logic gate besides the multiplexer is used.

<em>H</em>(<em>A</em>,<em>B</em>,<em>C</em>,<em>D</em>) = m(2, 7, 10, 12, 14, 15)

The block diagram of a 4:1 multiplexer is given in part (a) above.







<ul>

 <li>Implement the following Boolean function using a single 2×4 decoder with one-enable and active high outputs, and at most one logic gate.</li>

</ul>

<em>G</em>(<em>A</em>,<em>B</em>,<em>C</em>,<em>D</em>) = m(2, 11)

The block diagram of a 2×4 decoder with one-enable and active high outputs is shown below.










<ul>

 <li>Below is a partial function table of an 8-to-3 priority encoder. It consists of 8 inputs (<em>A</em><sub>7</sub> to <em>A</em><sub>0</sub>) and 3 outputs (<em>F</em><sub>2</sub> to <em>F</em><sub>0</sub>). <em>A<sub>i</sub></em> has higher priority than <em>A<sub>j</sub></em> for <em>i</em> &gt; <em>j</em>. The only invalid input combination occurs when all inputs are zeroes. ‘X’ represents don’t-care. Write out the simplified SOP expressions for <em>F</em><sub>2</sub>, <em>F</em><sub>1 </sub>and <em>F</em><sub>0</sub>.</li>

</ul>







<strong>             </strong>

<h1>Question 2. Sequential Circuit</h1>

Analyze the following sequential circuit with JK flip-flops, an input <em>x</em> and an output <em>z</em>. The states are represented by <em>ABC</em>.




Complete the state diagram for the circuit below. States are shown in decimal and the labels are in <em>x</em>/<em>z</em> format, where <em>x</em> is the input and <em>z</em> the output. Two arrows have been drawn for you. For ease of tracing, place a label near the start of its associated arrow. Use the same positions of the states in the diagram below to ease grading.







<h1>Question 3. Pipelining</h1>

(Past year’s exam question)

The following MIPS code reads an integer array <strong><em>A</em></strong>, whose base address is stored in <strong>$s0</strong>, and computes some answer in <strong>$s2</strong>. The register <strong>$s1</strong> is associated with the integer variable <strong>cutoff</strong>.

<strong>        addi $s2, $zero, 0     # Inst1:</strong> <strong>count = 0 </strong><strong>        addi $t0, $s0, 40      # Inst2:</strong> <strong>$t0 pts to A[10]</strong><strong>                                #</strong><strong>        </strong><strong>i = 9,8,…,0</strong> <strong>  Here: addi $t0, $t0, -4      # Inst3:</strong> <strong>$t0 pts to A[i]</strong><strong>         lw   $t1, 0($t0)       # Inst4:</strong> <strong>$t1 = A[i]</strong> <strong>        slt  $t2, $t1, $s1     # Inst5:</strong> <strong>if (A[i]&lt;cutoff)</strong><strong>         beq  $t2, $zero, Skip  # Inst6:</strong> <strong>{</strong><strong>          addi $s2, $s2, 1       # Inst7:</strong><strong>   count++;  }</strong><strong>   Skip: beq  $t0, $s0, Fin     # Inst8:</strong> <strong>$t0 pts to A[0]?</strong><strong>         j    Here              # Inst9   Fin: </strong>




For parts (a) to (c) below, you are to calculate the total number of cycles required to complete the <u>first iteration</u> of the above code in a 5-stage MIPS pipeline, that is, instruction 1 through instruction 9. You need to count until the last stage (WB stage) of instruction 9. You may assume that all elements in array <em>A</em> have values that are smaller than <strong>cutoff</strong>.

<ul>

 <li>In an ideal pipeline with no delays, how many cycles are needed to complete the first iteration of the code?</li>

 <li>Assume without forwarding and branch is resolved at stage 4 (MEM) stage. No branch prediction is made and no delayed branching is used. What is the total number of cycles required to complete the first iteration of the code?</li>

 <li>Assume with forwarding and branch is resolved at stage 2 (ID) stage. No branch prediction is made and no delayed branching is used. What is the total number of cycles required to complete the first iteration of the code?</li>

</ul>

For a general array (where the array elements have random values instead of all being smaller than <strong>cutoff</strong>), how would the choice of branch prediction (that is, choosing between “branch taken” and “branch not taken”) affect the performance of this code with respect to the beq instruction in instruction 6?