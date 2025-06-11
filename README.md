# comp311-lab-2-solved
**TO GET THIS SOLUTION VISIT:** [Comp311 Lab 2 Solved](https://mantutor.com/product/comp311-now-that-we-are-familiar-and-comfortable-with-wiring-combinational-logic-circuits-in-digital-its-time-to-build-some-sequential-logic-circuits-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115126&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Comp311 Lab 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 138px;">
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
            5/5 - (1 vote)    </div>
    </div>
Now that we are familiar and comfortable with wiring combinational logic circuits in Digital, it’s time to build some sequential logic circuits.

Sequential logic circuits are the backbone of constructing finite-state machines, a topic you will cover in Comp 455. Here’s a blurb from Wikipedia that explains the usefullness of sequential logic circuits:

Sequential logic is a type of logic circuit whose output depends not only on the present value of its input signals but on the sequence of past inputs, the input history as well. This is in contrast to combinational logic, whose output is a function of only the present input.

That is, sequential logic has state (memory) while combinational logic does not.

A great example of sequential logic is below:

A familiar example of a device with sequential logic is a television set with “channel up” and “channel down” buttons. Pressing the “up” button gives the television an input telling it to switch to the next channel above the one it is currently receiving. If the television is on channel 5, pressing “up” switches it to receive channel 6. However, if the television is on channel 8, pressing “up” switches it to channel “9”. In order for the channel selection to operate correctly, the television must be aware of which channel it is currently receiving, which was determined by past channel selections. The television stores the current channel as part of its state. When a “channel up” or “channel down” input is given to it, the sequential logic of the channel selection circuitry calculates the new channel from the input and the current channel.

Objective

Our goal for this lab is to create a 3-bit counter. Essentially, we want to design a circuit that “counts” upwards, from 0 to 7. Electronic counters come in two types: Asynchronous and Synchronous. In this lab we will build a Synchronous counter. Synchronous counters use a common clock and logic between their components to encode the count sequence. In these types of counters, the flip-flops are clocked at the same time by a common clock pulse. Thus, all the flip-flops change state simultaneously (in parallel). The counter advances upward in sequence (0, 1, 2, 3, 4, 5, 6, 7). The counter advances to the next output state on the positive edge of the input clock.

State Diagram

The next step in designing our 3-bit circuit is to design a State Diagram. This is a diagram that is made from circles and arrows and describes visually the operation of our circuit. In mathematic terms, this diagram that describes the operation of our sequential circuit is a Finite State Machine.

The state diagram of our circuit is shown to the right. Every circle represents a

So, what does our â€œMachineâ€ do exactly? It starts from the â€œ000â€ state and waits until a 1 is read at the input. Then it goes to the â€œ001â€ state. As our clock continues, the circuit goes to the third state, “010â€, and so on. Note that if the input to a state is 0, the machine stays in it’s current state. This gives us the functionality of advancing to the next output state on the positive edge of the input clock or “pausing” the clock and remaining in the current state.

We will come back to analyzing this state diagram soon.

T Flip-Flops

There are indeed many ways to make a 3-bit counter. You can use D or JK flip-flops, but in this lab we will use a T flip-flop. You should have learned about D flip-flops in class, and hopefully this lab will expose you to a different type of flip-flop, the T flip-flop.

There are many different types of flip-flops; however, they are all sensitive to clock edges, but they perform different actions in response to the input states. The â€œTâ€ in â€œT flip-flopâ€ stands for â€œtoggle.â€ When you toggle a light switch, you are changing from one state (on or off) to the other state (off or on). This is equivalent to what happens when you provide a logic-high input to a T flip-flop: if the output is currently logic high, it changes to logic low; if itâ€™s currently logic low, it changes to logic high. A logic-low input causes the T flip-flop to maintain its current output state.

To-Do:

Truth-Table Based on State Diagram

For our 3-bit counter we’re going to need 3 T flip-flops! Each output of a T flip-flop will be one binary digit of our number (0-7). What we need is to create a truth table that displays the current state, output states, and values of T based on our state diagram. Using the state diagram previosuly displayed in the lab, fill in these values. Q represents the current state, Q* represents the next state, and Ti represents the input to the flip-flop. Fill out the file “state-diagram-truth-table.csv” with the completed table.

Let’s give a little more information to make sure the concept is completely clear.

C, B, A -&gt; Represent the binary digits of the numbers we are counting. Ex. 001 -&gt; 1, 010 -&gt; 2, 100 -&gt; 4, and so on. For 001, C -&gt; 0, B -&gt; 0, 1

-&gt; A

QC, QB, QA -&gt; Represent the current state of our machine. Ex. 101 means that QC -&gt; 1, QB -&gt; 0, QC -&gt; 1. If 101 is the current state of the machine, then what are the possible next states? 101 can either transition to 101 (stay the same) or to 110 (increase to 6). That means in our truth table we will have 2 rows where QC, QB, QA are 101 respectively. The QC QB QA* for one row will be 101 (stay the same; input = 0 ) and another row will be 110 (change states; input = 1).

To-Do:

(notice input 0 and input 1)*

ie.

|1 |0 |0 |1 |0 |0 |1 |

These will be the first two rows of your truth table. Notice how the first row represents the output state when the machine does not change states, and the second row is moving to the next state.

K-Maps

To-Do:

| | QA Input(Y) | |——-|—-| |QC QB| value of Ti |

Implementation:

Now that we have our three expressions representing what the input “T” should be for each of our T flip-flops, it’s time to wire it up in Digital. I’d recommend drawing the circuit on paper first

Create a file called “Lab02.dig” to build your circuit. You can find the flip-flop you need under components -&gt; Flip-Flops -&gt; T-Flip-Flop. You’ll also need a clock for this assignment. Find the clock under components -&gt; IO -&gt; clock input. When you place your clock make sure to right-click (control-click on mac) and check the box labeled “start real time clock”.

To-Do:

Compelete the circuit needed to wire up the 3-bit counter. The “T” input is what you solved for in the k-map. “Q” is the output of that digit. Ignore Q-bar, its just the inverse of Q. Each output Q of the three T-Flip-Flops should be connected to an output component. Label each of your output components as QC, QB, and QA respectively. You should also label your input component “Y”. You must also label your clock component “CLK”.

At this point, when you start the simulation you should see the output components start to turn on and off in a fashion that counts upwards (only when the input Y is set to 1, when input Y is set to 0, the clock should hold steady in it’s current state).

Now the fun part: Create a file called “Lab02fun.dig”. Copy your circuit from “Lab02.dig” and paste it into this file. Also, copy your entire circuit from the previous Lab 1 (the seven segment display) and paste it into this document. Now instead of sending the Q outputs to an output component we’re going to send them to the inputs of the 7-segment display to watch our machine count!

Step 1: Delete inputs B, C, and D in the Lab01 circuit Step 2: Remove the output components for QC QB and QA from the Lab02 circuit Step 3: Connect output QC to where your old input B was to the Lab01 circuit Step 4: Connect output QB to where your old input C was to the Lab01 circuit Step 5: Connect output QA to where your old input D was to the Lab01 circuit

Now when you start the simulation you should be able to watch the 7-segment display also count up (Only when input y is set to 1. If y is set to 0 you should see the 7-segment display hold steady in it’s current state)! This is also a great way to ensure your circuits are correct.

When you finish save and commit all your changes!

Submit your assignment

Assignment submissions will be made through GradeScope.

1. Submit modifications using the commit Github Desktop instructions.

2. Update remote (origin) repository using the push Github Desktop instructions.

3. Go to the COMP 311 course in GradeScope and click on the assignment called Lab 01.

5. You should see a list of your public repositories. Select the one named lab-02-yourname and submit it.

6. Your assignment should be autograded within a few seconds and you will receive feedback.
