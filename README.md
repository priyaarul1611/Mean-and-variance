# Mean-and-variance

EXPT.NO.8	SIMULATION OF MEAN AND VARIANCE USING SCILAB

AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

EQUIPMENTS Needed

•	Computer with i3 Processor
•	SCI LAB

Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation

   PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated results

PROGRAM:
```
function X=f(x)
z=6*(1-x) **2;
 X=x*z;
endfunction
a=0;
b=1;
EX=intg(a,b,f);
function Y=c(y)
z=6*(1-y) **2;
Y=y*z;
endfunction
EY=intg(a,b,c);
disp(EX,"i)Mean of X=")
disp(EY,"Mean of  Y=")

function X=g(x)
z=6*(1-x) **2;
X=x**2 *z;
endfunction
a=0;
b=1;
EX2=intg(a,b,g);
function Y=h(y)
z=6*(1-y)**2;
Y=y**2 *z;
endfunction
EY2=intg(a,b,h);
vX2=EX2-(EX) **2;
vY2=EY2-(EY) **2;
disp(vX2,"ii)Variance of X");
disp(vY2,"Variance of Y");

x=input("type in the reference sequence=");
y=input("type in the reference sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```

OUTPUT

1.Mean of X=0.5
  Mean of y=0.5

2.Variance of x:-0.05
  Variance of y:-0.05

Cross correlation
Type in the reference sequence =[1 2 3 4 5 6 7 8]
Type in the second sequence = [9 8 7 6 5 4 3 2 1]

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/16133882-c4c0-40a1-9dc7-0f8e7e02041b" />

RESULT: 
Thus, the mean, variance and cross correlation are executed in Scilab and output is verified.



