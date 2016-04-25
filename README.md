# Turing-Machine-Simulation
Computer Theory project 

### How to use 
if you want to add machine just go to `MachinesLibrary.java class`

and add your own machine as :

```java
 TuringMachine newTM = new TuringMachine();
		newTM.addState("q1");
		newTM.addState("q2");
		newTM.addState("q3");
		newTM.addState("q4");
		newTM.addState("q5");
		newTM.addState("q6");
		newTM.addState("q7");
		newTM.addState("q8");
		newTM.addState("qa");
		newTM.addState("qr");
		newTM.setStartState("q1");
		newTM.setAcceptState("qa");
		newTM.setRejectState("qr");
		newTM.addTransition("q1", '1', "q3", 'x', true);
		newTM.addTransition("q1", '0', "q2", 'x', true);
		newTM.addTransition("q1", '#', "q8", '#', true);
		newTM.addTransition("q2", '0', "q2", '0', true);
		newTM.addTransition("q2", '1', "q2", '1', true);
		newTM.addTransition("q2", '#', "q4", '#', true);
		newTM.addTransition("q3", '0', "q3", '0', true);
		newTM.addTransition("q3", '1', "q3", '1', true);
		newTM.addTransition("q3", '#', "q5", '#', true);
		newTM.addTransition("q4", 'x', "q4", 'x', true);
		newTM.addTransition("q4", '0', "q6", 'x', false);
		newTM.addTransition("q5", 'x', "q5", 'x', true);
		newTM.addTransition("q5", '1', "q6", 'x', false);
		newTM.addTransition("q6", '0', "q6", '0', false);
		newTM.addTransition("q6", '1', "q6", '1', false);
		newTM.addTransition("q6", 'x', "q6", 'x', false);
		newTM.addTransition("q6", '#', "q7", '#', false);
		newTM.addTransition("q7", '0', "q7", '0', false);
		newTM.addTransition("q7", '1', "q7", '1', false);
		newTM.addTransition("q7", 'x', "q1", 'x', true);
		newTM.addTransition("q8", 'x', "q8", 'x', true);
		newTM.addTransition("q8", '_', "qa", '_', true);
		return newTM;
```
###### input and outPut
- input some thing seem as `010000110101#010000110101`
- out put will seem as
```
q1 010000110101#010000110101
x q2 10000110101#010000110101
x1 q2 0000110101#010000110101
x10 q2 000110101#010000110101
x100 q2 00110101#010000110101
x1000 q2 0110101#010000110101
x10000 q2 110101#010000110101
x100001 q2 10101#010000110101
x1000011 q2 0101#010000110101
x10000110 q2 101#010000110101
x100001101 q2 01#010000110101
x1000011010 q2 1#010000110101
x10000110101 q2 #010000110101
x10000110101# q4 010000110101
x10000110101 q6 #x10000110101
x1000011010 q7 1#x10000110101
x100001101 q7 01#x10000110101
x10000110 q7 101#x10000110101
x1000011 q7 0101#x10000110101
x100001 q7 10101#x10000110101
x10000 q7 110101#x10000110101
x1000 q7 0110101#x10000110101
x100 q7 00110101#x10000110101
x10 q7 000110101#x10000110101
x1 q7 0000110101#x10000110101
x q7 10000110101#x10000110101
 q7 x10000110101#x10000110101
x q1 10000110101#x10000110101
xx q3 0000110101#x10000110101
xx0 q3 000110101#x10000110101
xx00 q3 00110101#x10000110101
xx000 q3 0110101#x10000110101
xx0000 q3 110101#x10000110101
xx00001 q3 10101#x10000110101
xx000011 q3 0101#x10000110101
xx0000110 q3 101#x10000110101
xx00001101 q3 01#x10000110101
xx000011010 q3 1#x10000110101
xx0000110101 q3 #x10000110101
xx0000110101# q5 x10000110101
xx0000110101#x q5 10000110101
xx0000110101# q6 xx0000110101
xx0000110101 q6 #xx0000110101
xx000011010 q7 1#xx0000110101
xx00001101 q7 01#xx0000110101
xx0000110 q7 101#xx0000110101
xx000011 q7 0101#xx0000110101
xx00001 q7 10101#xx0000110101
xx0000 q7 110101#xx0000110101
xx000 q7 0110101#xx0000110101
xx00 q7 00110101#xx0000110101
xx0 q7 000110101#xx0000110101
xx q7 0000110101#xx0000110101
x q7 x0000110101#xx0000110101
xx q1 0000110101#xx0000110101
xxx q2 000110101#xx0000110101
xxx0 q2 00110101#xx0000110101
xxx00 q2 0110101#xx0000110101
xxx000 q2 110101#xx0000110101
xxx0001 q2 10101#xx0000110101
xxx00011 q2 0101#xx0000110101
xxx000110 q2 101#xx0000110101
xxx0001101 q2 01#xx0000110101
xxx00011010 q2 1#xx0000110101
xxx000110101 q2 #xx0000110101
xxx000110101# q4 xx0000110101
xxx000110101#x q4 x0000110101
xxx000110101#xx q4 0000110101
xxx000110101#x q6 xx000110101
xxx000110101# q6 xxx000110101
xxx000110101 q6 #xxx000110101
xxx00011010 q7 1#xxx000110101
xxx0001101 q7 01#xxx000110101
xxx000110 q7 101#xxx000110101
xxx00011 q7 0101#xxx000110101
xxx0001 q7 10101#xxx000110101
xxx000 q7 110101#xxx000110101
xxx00 q7 0110101#xxx000110101
xxx0 q7 00110101#xxx000110101
xxx q7 000110101#xxx000110101
xx q7 x000110101#xxx000110101
xxx q1 000110101#xxx000110101
xxxx q2 00110101#xxx000110101
xxxx0 q2 0110101#xxx000110101
xxxx00 q2 110101#xxx000110101
xxxx001 q2 10101#xxx000110101
xxxx0011 q2 0101#xxx000110101
xxxx00110 q2 101#xxx000110101
xxxx001101 q2 01#xxx000110101
xxxx0011010 q2 1#xxx000110101
xxxx00110101 q2 #xxx000110101
xxxx00110101# q4 xxx000110101
xxxx00110101#x q4 xx000110101
xxxx00110101#xx q4 x000110101
xxxx00110101#xxx q4 000110101
xxxx00110101#xx q6 xx00110101
xxxx00110101#x q6 xxx00110101
xxxx00110101# q6 xxxx00110101
xxxx00110101 q6 #xxxx00110101
xxxx0011010 q7 1#xxxx00110101
xxxx001101 q7 01#xxxx00110101
xxxx00110 q7 101#xxxx00110101
xxxx0011 q7 0101#xxxx00110101
xxxx001 q7 10101#xxxx00110101
xxxx00 q7 110101#xxxx00110101
xxxx0 q7 0110101#xxxx00110101
xxxx q7 00110101#xxxx00110101
xxx q7 x00110101#xxxx00110101
xxxx q1 00110101#xxxx00110101
xxxxx q2 0110101#xxxx00110101
xxxxx0 q2 110101#xxxx00110101
xxxxx01 q2 10101#xxxx00110101
xxxxx011 q2 0101#xxxx00110101
xxxxx0110 q2 101#xxxx00110101
xxxxx01101 q2 01#xxxx00110101
xxxxx011010 q2 1#xxxx00110101
xxxxx0110101 q2 #xxxx00110101
xxxxx0110101# q4 xxxx00110101
xxxxx0110101#x q4 xxx00110101
xxxxx0110101#xx q4 xx00110101
xxxxx0110101#xxx q4 x00110101
xxxxx0110101#xxxx q4 00110101
xxxxx0110101#xxx q6 xx0110101
xxxxx0110101#xx q6 xxx0110101
xxxxx0110101#x q6 xxxx0110101
xxxxx0110101# q6 xxxxx0110101
xxxxx0110101 q6 #xxxxx0110101
xxxxx011010 q7 1#xxxxx0110101
xxxxx01101 q7 01#xxxxx0110101
xxxxx0110 q7 101#xxxxx0110101
xxxxx011 q7 0101#xxxxx0110101
xxxxx01 q7 10101#xxxxx0110101
xxxxx0 q7 110101#xxxxx0110101
xxxxx q7 0110101#xxxxx0110101
xxxx q7 x0110101#xxxxx0110101
xxxxx q1 0110101#xxxxx0110101
xxxxxx q2 110101#xxxxx0110101
xxxxxx1 q2 10101#xxxxx0110101
xxxxxx11 q2 0101#xxxxx0110101
xxxxxx110 q2 101#xxxxx0110101
xxxxxx1101 q2 01#xxxxx0110101
xxxxxx11010 q2 1#xxxxx0110101
xxxxxx110101 q2 #xxxxx0110101
xxxxxx110101# q4 xxxxx0110101
xxxxxx110101#x q4 xxxx0110101
xxxxxx110101#xx q4 xxx0110101
xxxxxx110101#xxx q4 xx0110101
xxxxxx110101#xxxx q4 x0110101
xxxxxx110101#xxxxx q4 0110101
xxxxxx110101#xxxx q6 xx110101
xxxxxx110101#xxx q6 xxx110101
xxxxxx110101#xx q6 xxxx110101
xxxxxx110101#x q6 xxxxx110101
xxxxxx110101# q6 xxxxxx110101
xxxxxx110101 q6 #xxxxxx110101
xxxxxx11010 q7 1#xxxxxx110101
xxxxxx1101 q7 01#xxxxxx110101
xxxxxx110 q7 101#xxxxxx110101
xxxxxx11 q7 0101#xxxxxx110101
xxxxxx1 q7 10101#xxxxxx110101
xxxxxx q7 110101#xxxxxx110101
xxxxx q7 x110101#xxxxxx110101
xxxxxx q1 110101#xxxxxx110101
xxxxxxx q3 10101#xxxxxx110101
xxxxxxx1 q3 0101#xxxxxx110101
xxxxxxx10 q3 101#xxxxxx110101
xxxxxxx101 q3 01#xxxxxx110101
xxxxxxx1010 q3 1#xxxxxx110101
xxxxxxx10101 q3 #xxxxxx110101
xxxxxxx10101# q5 xxxxxx110101
xxxxxxx10101#x q5 xxxxx110101
xxxxxxx10101#xx q5 xxxx110101
xxxxxxx10101#xxx q5 xxx110101
xxxxxxx10101#xxxx q5 xx110101
xxxxxxx10101#xxxxx q5 x110101
xxxxxxx10101#xxxxxx q5 110101
xxxxxxx10101#xxxxx q6 xx10101
xxxxxxx10101#xxxx q6 xxx10101
xxxxxxx10101#xxx q6 xxxx10101
xxxxxxx10101#xx q6 xxxxx10101
xxxxxxx10101#x q6 xxxxxx10101
xxxxxxx10101# q6 xxxxxxx10101
xxxxxxx10101 q6 #xxxxxxx10101
xxxxxxx1010 q7 1#xxxxxxx10101
xxxxxxx101 q7 01#xxxxxxx10101
xxxxxxx10 q7 101#xxxxxxx10101
xxxxxxx1 q7 0101#xxxxxxx10101
xxxxxxx q7 10101#xxxxxxx10101
xxxxxx q7 x10101#xxxxxxx10101
xxxxxxx q1 10101#xxxxxxx10101
xxxxxxxx q3 0101#xxxxxxx10101
xxxxxxxx0 q3 101#xxxxxxx10101
xxxxxxxx01 q3 01#xxxxxxx10101
xxxxxxxx010 q3 1#xxxxxxx10101
xxxxxxxx0101 q3 #xxxxxxx10101
xxxxxxxx0101# q5 xxxxxxx10101
xxxxxxxx0101#x q5 xxxxxx10101
xxxxxxxx0101#xx q5 xxxxx10101
xxxxxxxx0101#xxx q5 xxxx10101
xxxxxxxx0101#xxxx q5 xxx10101
xxxxxxxx0101#xxxxx q5 xx10101
xxxxxxxx0101#xxxxxx q5 x10101
xxxxxxxx0101#xxxxxxx q5 10101
xxxxxxxx0101#xxxxxx q6 xx0101
xxxxxxxx0101#xxxxx q6 xxx0101
xxxxxxxx0101#xxxx q6 xxxx0101
xxxxxxxx0101#xxx q6 xxxxx0101
xxxxxxxx0101#xx q6 xxxxxx0101
xxxxxxxx0101#x q6 xxxxxxx0101
xxxxxxxx0101# q6 xxxxxxxx0101
xxxxxxxx0101 q6 #xxxxxxxx0101
xxxxxxxx010 q7 1#xxxxxxxx0101
xxxxxxxx01 q7 01#xxxxxxxx0101
xxxxxxxx0 q7 101#xxxxxxxx0101
xxxxxxxx q7 0101#xxxxxxxx0101
xxxxxxx q7 x0101#xxxxxxxx0101
xxxxxxxx q1 0101#xxxxxxxx0101
xxxxxxxxx q2 101#xxxxxxxx0101
xxxxxxxxx1 q2 01#xxxxxxxx0101
xxxxxxxxx10 q2 1#xxxxxxxx0101
xxxxxxxxx101 q2 #xxxxxxxx0101
xxxxxxxxx101# q4 xxxxxxxx0101
xxxxxxxxx101#x q4 xxxxxxx0101
xxxxxxxxx101#xx q4 xxxxxx0101
xxxxxxxxx101#xxx q4 xxxxx0101
xxxxxxxxx101#xxxx q4 xxxx0101
xxxxxxxxx101#xxxxx q4 xxx0101
xxxxxxxxx101#xxxxxx q4 xx0101
xxxxxxxxx101#xxxxxxx q4 x0101
xxxxxxxxx101#xxxxxxxx q4 0101
xxxxxxxxx101#xxxxxxx q6 xx101
xxxxxxxxx101#xxxxxx q6 xxx101
xxxxxxxxx101#xxxxx q6 xxxx101
xxxxxxxxx101#xxxx q6 xxxxx101
xxxxxxxxx101#xxx q6 xxxxxx101
xxxxxxxxx101#xx q6 xxxxxxx101
xxxxxxxxx101#x q6 xxxxxxxx101
xxxxxxxxx101# q6 xxxxxxxxx101
xxxxxxxxx101 q6 #xxxxxxxxx101
xxxxxxxxx10 q7 1#xxxxxxxxx101
xxxxxxxxx1 q7 01#xxxxxxxxx101
xxxxxxxxx q7 101#xxxxxxxxx101
xxxxxxxx q7 x101#xxxxxxxxx101
xxxxxxxxx q1 101#xxxxxxxxx101
xxxxxxxxxx q3 01#xxxxxxxxx101
xxxxxxxxxx0 q3 1#xxxxxxxxx101
xxxxxxxxxx01 q3 #xxxxxxxxx101
xxxxxxxxxx01# q5 xxxxxxxxx101
xxxxxxxxxx01#x q5 xxxxxxxx101
xxxxxxxxxx01#xx q5 xxxxxxx101
xxxxxxxxxx01#xxx q5 xxxxxx101
xxxxxxxxxx01#xxxx q5 xxxxx101
xxxxxxxxxx01#xxxxx q5 xxxx101
xxxxxxxxxx01#xxxxxx q5 xxx101
xxxxxxxxxx01#xxxxxxx q5 xx101
xxxxxxxxxx01#xxxxxxxx q5 x101
xxxxxxxxxx01#xxxxxxxxx q5 101
xxxxxxxxxx01#xxxxxxxx q6 xx01
xxxxxxxxxx01#xxxxxxx q6 xxx01
xxxxxxxxxx01#xxxxxx q6 xxxx01
xxxxxxxxxx01#xxxxx q6 xxxxx01
xxxxxxxxxx01#xxxx q6 xxxxxx01
xxxxxxxxxx01#xxx q6 xxxxxxx01
xxxxxxxxxx01#xx q6 xxxxxxxx01
xxxxxxxxxx01#x q6 xxxxxxxxx01
xxxxxxxxxx01# q6 xxxxxxxxxx01
xxxxxxxxxx01 q6 #xxxxxxxxxx01
xxxxxxxxxx0 q7 1#xxxxxxxxxx01
xxxxxxxxxx q7 01#xxxxxxxxxx01
xxxxxxxxx q7 x01#xxxxxxxxxx01
xxxxxxxxxx q1 01#xxxxxxxxxx01
xxxxxxxxxxx q2 1#xxxxxxxxxx01
xxxxxxxxxxx1 q2 #xxxxxxxxxx01
xxxxxxxxxxx1# q4 xxxxxxxxxx01
xxxxxxxxxxx1#x q4 xxxxxxxxx01
xxxxxxxxxxx1#xx q4 xxxxxxxx01
xxxxxxxxxxx1#xxx q4 xxxxxxx01
xxxxxxxxxxx1#xxxx q4 xxxxxx01
xxxxxxxxxxx1#xxxxx q4 xxxxx01
xxxxxxxxxxx1#xxxxxx q4 xxxx01
xxxxxxxxxxx1#xxxxxxx q4 xxx01
xxxxxxxxxxx1#xxxxxxxx q4 xx01
xxxxxxxxxxx1#xxxxxxxxx q4 x01
xxxxxxxxxxx1#xxxxxxxxxx q4 01
xxxxxxxxxxx1#xxxxxxxxx q6 xx1
xxxxxxxxxxx1#xxxxxxxx q6 xxx1
xxxxxxxxxxx1#xxxxxxx q6 xxxx1
xxxxxxxxxxx1#xxxxxx q6 xxxxx1
xxxxxxxxxxx1#xxxxx q6 xxxxxx1
xxxxxxxxxxx1#xxxx q6 xxxxxxx1
xxxxxxxxxxx1#xxx q6 xxxxxxxx1
xxxxxxxxxxx1#xx q6 xxxxxxxxx1
xxxxxxxxxxx1#x q6 xxxxxxxxxx1
xxxxxxxxxxx1# q6 xxxxxxxxxxx1
xxxxxxxxxxx1 q6 #xxxxxxxxxxx1
xxxxxxxxxxx q7 1#xxxxxxxxxxx1
xxxxxxxxxx q7 x1#xxxxxxxxxxx1
xxxxxxxxxxx q1 1#xxxxxxxxxxx1
xxxxxxxxxxxx q3 #xxxxxxxxxxx1
xxxxxxxxxxxx# q5 xxxxxxxxxxx1
xxxxxxxxxxxx#x q5 xxxxxxxxxx1
xxxxxxxxxxxx#xx q5 xxxxxxxxx1
xxxxxxxxxxxx#xxx q5 xxxxxxxx1
xxxxxxxxxxxx#xxxx q5 xxxxxxx1
xxxxxxxxxxxx#xxxxx q5 xxxxxx1
xxxxxxxxxxxx#xxxxxx q5 xxxxx1
xxxxxxxxxxxx#xxxxxxx q5 xxxx1
xxxxxxxxxxxx#xxxxxxxx q5 xxx1
xxxxxxxxxxxx#xxxxxxxxx q5 xx1
xxxxxxxxxxxx#xxxxxxxxxx q5 x1
xxxxxxxxxxxx#xxxxxxxxxxx q5 1
xxxxxxxxxxxx#xxxxxxxxxx q6 xx
xxxxxxxxxxxx#xxxxxxxxx q6 xxx
xxxxxxxxxxxx#xxxxxxxx q6 xxxx
xxxxxxxxxxxx#xxxxxxx q6 xxxxx
xxxxxxxxxxxx#xxxxxx q6 xxxxxx
xxxxxxxxxxxx#xxxxx q6 xxxxxxx
xxxxxxxxxxxx#xxxx q6 xxxxxxxx
xxxxxxxxxxxx#xxx q6 xxxxxxxxx
xxxxxxxxxxxx#xx q6 xxxxxxxxxx
xxxxxxxxxxxx#x q6 xxxxxxxxxxx
xxxxxxxxxxxx# q6 xxxxxxxxxxxx
xxxxxxxxxxxx q6 #xxxxxxxxxxxx
xxxxxxxxxxx q7 x#xxxxxxxxxxxx
xxxxxxxxxxxx q1 #xxxxxxxxxxxx
xxxxxxxxxxxx# q8 xxxxxxxxxxxx
xxxxxxxxxxxx#x q8 xxxxxxxxxxx
xxxxxxxxxxxx#xx q8 xxxxxxxxxx
xxxxxxxxxxxx#xxx q8 xxxxxxxxx
xxxxxxxxxxxx#xxxx q8 xxxxxxxx
xxxxxxxxxxxx#xxxxx q8 xxxxxxx
xxxxxxxxxxxx#xxxxxx q8 xxxxxx
xxxxxxxxxxxx#xxxxxxx q8 xxxxx
xxxxxxxxxxxx#xxxxxxxx q8 xxxx
xxxxxxxxxxxx#xxxxxxxxx q8 xxx
xxxxxxxxxxxx#xxxxxxxxxx q8 xx
xxxxxxxxxxxx#xxxxxxxxxxx q8 x
xxxxxxxxxxxx#xxxxxxxxxxxx q8 _
The input was accepted.
```
