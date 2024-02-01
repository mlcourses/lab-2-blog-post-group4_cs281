# Lab 2: Building a 2-1 Mux, 4-1 Mux and a Cascade Adder

## Overview and Motivation
  This week we began to build functional multiplexors and adders using the logic gates we were introduced to last week. We designed and built a 2-1 mux, a 4-1 mux - which we automatically tested with our Arduino, and a 1 bit adder. Through these exercises, we saw real-world application of the logic gates, circuits, and truth tables which we have been studying in class.

## Materials
1. PB-503 (breadboard)
2. Electrical Wires
3. Arduino Kit
4. 7404 NOT Gate
5. 7408 AND Gate
6. 7486 XOR Gate
7. 74150 16-1 Multiplexor

## Project Steps

PART 1: 2-1 MULTIPLEXOR

  In the prelab for this lab, we designed a 2-1 multiplexor circuit using a NOT gate, 2 AND gates, and an OR gate. A 2-1 multiplexor takes two binary data inputs, and one binary selector input, and it allows a user to select which of the two data inputs will be passed through to the output. We took the truth table for this circuit, which had our desired outputs given the three input variables, and used Sum-Of-Products design to find the boolean expression for the mux. This boolean expression is Y = A~S + BS. From this expression, we designed our circuit, which is pictured below. In part 1 of the lab, we implemented our design on the breadboard. 

![2-1 mux](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/122911760/c4931388-ec7f-46b2-a49d-eba6b3520ddb)


PART 2: 4-1 MULTIPLEXOR

  In this experiment, we used a 74150 and a not-gate chip. In the prelab for this experiment, we made a wiring diagram for this IC. It takes 4 data inputs and 2 selector inputs. We had the truth table for this circuit. Then we found the boolean expression for the mux which is C = Cin xor(A xor B) and Cout=Cin A+Cin B+AB. From this expression, we designed our circuit, which is pictured below. In part 1 of the lab, we implemented our design on the breadboard. 

![4-1 mux](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/122911760/46da525f-e531-4190-be3d-6eb435282c94)

PART 3: 4-1 MULTIPLEXOR WITH ARDUINO

  In this experiment, we keep the circuit we built in the last experiment but remove the wires to the switches and reconnect them to the Arduino board. We used the Arduino program from the lab instructions. The provided Arduino program is designed to test the operation of a 4-to-1 multiplexer (mux) using an Arduino board. The mux is controlled by the Arduino, which sets the data inputs, selects lines, reads the output from the mux, and compares it to the expected results.

![4-1 mux with arduino](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/122911760/62e628fd-a5b7-43b3-94f1-a57cc87ff0fd)

PART 4: 1 BIT ADDER

## Goal
The goal of this part is to build a cascade adder on the breadboard. A cascade adder is one that accepts 3 inputs, 2 1-bit binary number (A and B) and a "carry on" variable (Cin) and outputs the result (C) as well as any "carry on" (Cout) that overflows the adder (which can only display 2 bits). 

For example, if 01 (A) and 01 (B) are inserted into the adder with no carry on (Cin = 0), the result (C) would be 10 and the resultant carry on (Cout) would be 0. On the other hand, if 11 and 11 is inserted into the adder with no carry on (Cin = 0), the result if 11 + 11 will be 110. In this case, (C) would be 10 and the resultant carry on (Cout) would be 1.

## Procedures
From the example above, we were able to make a truth table of the possible values of A, B and Cin and then mapped these to the results of C and Cout. This resulted in the following table.
![IMG_C646DC305C09-1](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/b80024d9-0865-4a9e-b77e-dee7584174b3)

Implementing SOP design onto the table, we wrote out the equation for a circuit that would result in C and another function that would result in Cout. We simplified it until we got the following equations:
![IMG_D4BAF3B9113C-1](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/e5c96602-901f-45b8-a353-f8ec64e248bf)
![IMG_A87ED35FDFD4-1](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/0350bd28-9204-45d1-9df3-fee995484d89)

From these equations, we were able to construct two circuits, one for C and one for Cin. We then drew these circuits on Logisim to test and see whether toggling A, B and Cin will result in the same results for C and Cout as displayed in the table.
<img width="530" alt="Untitled 2" src="https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/d50a2fab-8945-42b2-a6b1-8c12c7e8d37c">


After seeing that everything is correct, we combined the two circuits into one (because we only want one circuit on the breadboard). We also drew the circuit now with the diagrams of the logic gates we were going to use so we knew how to wire the logic gates. For example, the two circuits required a combination of 3 AND gates in the Logisim diagram but only one 7408 AND gate. This is because the 7408 gate actually has places for 8 inputs and 4 outputs. Thus, this step is very important as it is borderline impossible to build a circuit from the Logisim diagram above. We ended up with the wiring diagram below:
![IMG_4D81DD273393-1](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/813e4205-056e-46d3-9f04-e55643230005)

During the lab, we followed our wiring diagram above. There were an few niches though. We couldn't plug multiple plugs coming out of one logic switch, so what we settled on doing was connecting the logic switch to 1 row of the breadboard, and because the 5-column section of the breadboard is connected by rows, all the other slots in that row will have the same power as the logic switch. This meant we could have 5 wires coming out of each logic switch and we only needed 3. An example of this could be seen on the left side of the top left AND logic gate. We ended up with the circuit below.
![adder breadboard circuit](https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/68cf7d65-4425-44d4-aef8-715a0543186e)

## Conclusion
After finishing part 3, we learnt how to build a somewhat complex circuit that could output 2 variables. We also learnt how to combine 2 separate circuits together to make 1 and intuitively realized how to get multiple signals from one logic switch. This part also required a lot of "the result of this gate goes into the input as another gate" and being able to build this circuit helped us to intuitively understand more about circuit building in general.

## Testing

PART 1: 2-1 MULTIPLEXOR

  We tested our 2-1 mux by toggling our selector switch: S1, and our two data switches: S5 and S6, and then by looking at the output displayed on the Logic Indicators of our breadboard. If we select want to output data input A, for example, we set S1 to low, and then toggle S5 as desired. See the video below for operation of this circuit. Comparing our outputs to our truth table for a 2-1 mux, we can confirm that our circuit is functioning correctly. 

https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/122911760/e120a063-6a55-4464-a16d-56aff027e2be

PART 2: 4-1 MULTIPLEXOR

  We tested our 4-1 mux by toggling our selector switch: S1 and S2, and our four data switches: S5, S6, S7, and S8. Then we check the output displayed on the Logic Indicators of our breadboard. Please check the video below about the operation of this circuit. We compare the outputs to our truth table written in the prelab, and we can get the result that our circuit is built correctly.

https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/122911760/b3973261-fa25-4b01-86e0-f43193b3bc2e

PART 3: 4-1 MULTIPLEXOR WITH ARDUINO

  We connect the wires from the circuit to the Arduino board shown in the video and picture below. Then we try to run the Arduino program. By running this program on the Arduino and opening the Serial Monitor, we can observe the results of each test case to verify the correct operation of the mux and your circuit. If the output matches the expected output, it will display "OK"; otherwise, it will display "BAD." This program automates the testing process and helps ensure the proper functioning of your 4-to-1 mux circuit. At last, we get all outputs "OK" which means it's giving the expected outputs.

PART 4: 1 BIT ADDER

  We tested the circuit out in the following videos. Instead of intuitively thinking about what each result would make, we followed the truth table we created and tested the outputs with different A, B and Cin inputs. This ensured that we actually had the correct results. The following video shows and explains the testing:

https://github.com/mlcourses/lab-2-blog-post-group4_cs281/assets/67582698/cb97a5b2-4a8c-4f9e-b440-eaa1f1194366

## Conclusion for the Lab

In today's lab, we built our skills of designing and implementing circuits, specifically learning the intricacies of multiplexors and adders. We learned how to use Sum-of-Products to go from truth tables to boolean expressions, to theoretical circuit designs, and then to physical circuits on our breadboard.
