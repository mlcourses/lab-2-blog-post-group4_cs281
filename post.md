# Lab X: Doing stuff with hardware!

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

PART 3: 4-1 MULTIPLEXOR WITH ARDUINO

PART 4: 1 BIT ADDER

## Testing

PART 1: 2-1 MULTIPLEXOR

  We tested our 2-1 mux by toggling our selector switch: S1, and our two data switches: S5 and S6, and then by looking at the output displayed on the Logic Indicators of our breadboard. If we select want to output data input A, for example, we set S1 to low, and then toggle S5 as desired. See the video below for operation of this circuit. Comparing our outputs to our truth table for a 2-1 mux, we can confirm that our circuit is functioning correctly. 

PART 2: 4-1 MULTIPLEXOR

PART 3: 4-1 MULTIPLEXOR WITH ARDUINO

PART 4: 1 BIT ADDER

## Conclusion

  In today's lab, we built our skills of designing and implementing circuits, specifically learning the intricacies of multiplexors and adders. We learned how to use Sum-of-Products to go from truth tables to boolean expressions, to theoretical circuit designs, and then to physical circuits on our breadboard. Our major takeaways are as follows: 
1. 




