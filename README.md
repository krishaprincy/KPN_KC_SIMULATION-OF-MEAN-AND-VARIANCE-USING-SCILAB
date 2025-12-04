# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB

## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed

•	Computer with i3 Processor
•	SCI LAB


## Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results


## PROGRAM

```

// ----- Part 1: Mean of X and Y using integration -----
function X = f(x)
    z = 5 * (1 - x)^2;
    X = x * z;
endfunction

function Y = c(y)
    z = 5 * (1 - y)^2;
    Y = y * z;
endfunction

a = 2;
b = 3;

EX = intg(a, b, f);  // Mean of X
EY = intg(a, b, c);  // Mean of Y

disp(EX, "i) Mean of X =");
disp(EY, "Mean of Y =");

// ----- Part 2: Variance of X and Y -----
function X = g(x)
    z = 3 * (1 - x)^2;
    X = x^2 * z;
endfunction

function Y = h(y)
    z = 3 * (1 - y)^2;
    Y = y^2 * z;
endfunction

EX2 = intg(a, b, g);
EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp(vX2, "ii) Variance of X =");
disp(vY2, "Variance of Y =");

// ----- Part 3: Cross-correlation -----
x = input("Type in the reference sequence x = ");
y = input("Type in the reference sequence y = ");

n1 = length(y) - 1;
n2 = length(x) - 1;

r = corr(x, y, n1);

disp(r, "iii) Cross-correlation of x and y =");

// Plot cross-correlation
plot(r);
xtitle("Cross-Correlation of x and y", "Lag", "Correlation");

```

## CALCULATION

![WhatsApp Image 2025-12-04 at 20 05 10_258e1ed6](https://github.com/user-attachments/assets/ee4f8b2d-39be-4e70-8ebc-19ecf7c767b1)



## OUTPUT

![WhatsApp Image 2025-12-04 at 20 03 50_1bc569f0](https://github.com/user-attachments/assets/29198b9b-63b6-4d54-9c95-dfccd5f86261)





## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
