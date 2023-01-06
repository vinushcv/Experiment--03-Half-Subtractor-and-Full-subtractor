# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
```
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: vinush.cv
RegisterNumber:  22001897
*/
### halfsubtractor
module expthree(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff = (a^b);
assign borr = (~a&b);
endmodule

### fullsubtractor
module expthreeone(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
assign borr = (~a&(b^c)|(b&c));
assign diff = (a^b^c);
endmodule
```

## Output:
## Truthtable:
###FOR HALFSUBTRACTOR:

![truthtablehalfsub](https://user-images.githubusercontent.com/113975318/210934726-0ddd071a-4e2c-4348-8c35-c98c075f1ce3.png)

###FOR FULLSUBTRACTOR:
![ttfullsub](https://user-images.githubusercontent.com/113975318/210934783-5315603d-43ab-4f3d-96b0-517808ef651f.png)


##  RTL realization
###FOR HALFSUBTRACTOR:
![rtlhalfsub](https://user-images.githubusercontent.com/113975318/210934825-68849557-a276-4a24-b460-432a8035b4da.png)

###FOR FULLSUBTRACTOR:
![rtlfullsub](https://user-images.githubusercontent.com/113975318/210934848-2e374390-fe37-4262-8ffa-b4780ef5e305.png)


## Timing diagram 
###FOR HALFSUBTRACTOR:
![timinghalfsub](https://user-images.githubusercontent.com/113975318/210934884-f61d3be2-c570-47e4-9590-f106d559a76f.png)

###FOR FULLSUBTRACTOR:
![timingfullsub](https://user-images.githubusercontent.com/113975318/210934915-6fd17152-d198-46a7-b93e-b56d0043b376.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
