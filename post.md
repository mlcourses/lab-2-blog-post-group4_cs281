# Lab X: Doing stuff with hardware!

Please write a blog post describing your lab here.

This is just an example of how you might structure your blog post, feel free to edit as you wish. For example, you might divide the lab into different sections each with their own intro, instructions, results, and takeaways. Please see the rubric for details on how the post will be evaluated.

## Overview and Motivation
This week we'll explore...

## Materials
1. PB-503 (breadboard)
2. Electrical Wires
3. Arduino Kit
4. 7404 NOT Gate
5. 7408 AND Gate
6. 7486 XOR Gate
7. 74150 16-1 Multiplexor

## Project Steps

## Testing

## Conclusion

## Part 

3: Building an Adder

## Goal
The goal of this part is to build a cascade adder on the breadboard. A cascade adder is one that accepts 3 inputs, 2 1-bit binary number (A and B) and a "carry on" variable (Cin) and outputs the result (C) as well as any "carry on" (Cout) that overflows the adder (which can only display 2 bits). 

For example, if 01 (A) and 01 (B) are inserted into the adder with no carry on (Cin = 0), the result (C) would be 10 and the resultant carry on (Cout) would be 0. On the other hand, if 11 and 11 is inserted into the adder with no carry on (Cin = 0), the result if 11 + 11 will be 110. In this case, (C) would be 10 and the resultant carry on (Cout) would be 1.

## Procedures
From the example above, we were able to make a truth table of the possible values of A, B and Cin and then mapped these to the results of C and Cout. This resulted in the following table.

## Image of Adder Truth Table

Implementing SOP design onto the table, we wrote out the equation for a circuit that would result in C and another function that would result in Cout. We simplified it until we got the following equations:

## Image of C and Cin final equations

From these equations, we were able to construct two circuits, one for C and one for Cin. We then drew these circuits on Logisim to test and see whether toggling A, B and Cin will result in the same results for C and Cout as displayed in the table.

## Image of C and Cin Logisim circuit

After seeing that everything is correct, we combined the two circuits into one (because we only want one circuit on the breadboard). We also drew the circuit now with the diagrams of the logic gates we were going to use so we knew how to wire the logic gates. For example, the two circuits required a combination of 3 AND gates in the Logisim diagram but only one 7408 AND gate. This is because the 7408 gate actually has places for 8 inputs and 4 outputs. Thus, this step is very important as it is borderline impossible to build a circuit from the Logisim diagram above. We ended up with the wiring diagram below:

## Image of Complete Wiring Diagram

During the lab, we followed our wiring diagram above. There were an few niches though. We couldn't plug multiple plugs coming out of one logic switch, so what we settled on doing was connecting the logic switch to 1 row of the breadboard, and because the 5-column section of the breadboard is connected by rows, all the other slots in that row will have the same power as the logic switch. This meant we could have 5 wires coming out of each logic switch and we only needed 3. An example of this could be seen on the left side of the top left AND logic gate. We ended up with the circuit below.

## Image of Complete Adder Circuit

## Testing
We tested the circuit out in the following videos. Instead of intuitively thinking about what each result would make, we followed the truth table we created and tested the outputs with different A, B and Cin inputs. This ensured that we actually had the correct results. The following video shows and explains the testing:

## Videos of Adder Testing

## Conclusion
After finishing part 3, we learnt how to build a somewhat complex circuit that could output 2 variables. We also learnt how to combine 2 separate circuits together to make 1 and intuitively realized how to get multiple signals from one logic switch. This part also required a lot of "the result of this gate goes into the input as another gate" and being able to build this circuit helped us to intuitively understand more about circuit building in general.
