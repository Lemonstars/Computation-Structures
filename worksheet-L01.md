## Information Content and Entropy

* A  
The 3-bit binary number can be 110 101 011  
p<sub>data</sub>=<sup>3</sup>/<sub>8</sub>  
I(X)=log<sub>2</sub><sup>8</sup>/<sub>3</sub> bits

* B  
The 3-bit binary number can be 101 011  
p<sub>data</sub>=<sup>2</sup>/<sub>8</sub>=<sup>1</sup>/<sub>4</sub>   
I(X)=log<sub>2</sub>4=2 bits  

* C  
H(X)=0.6\*log<sub>2</sub><sup>1</sup>/<sub>0.6</sub>+
0.4\*log<sub>2</sub><sup>1</sup>/<sub>0.4</sub>  

* D  
The decimal digit can be 0 3 6 9  
p<sub>data</sub>=<sup>4</sup>/<sub>10</sub>=<sup>2</sup>/<sub>5</sub>  
I(X)=log<sub>2</sub><sup>5</sup>/<sub>2</sub> bits  

* E  
I(X)=log<sub>2</sub><sup>2<sup>8</sup></sup>/<sub>8</sub>=5 bits

* F  
I(X)=log<sub>2</sub><sup>4</sup>/<sub>3</sub>  

* G  
H(X)=0.5\*log<sub>2</sub>2+0.125\*log<sub>2</sub>8+0.25\*log<sub>2</sub>4+
0.125\*log<sub>2</sub>8  
= 0.5+0.375+0.5+0.375  
= 1.75  

* H  
P<sub>data</sub>=<sup>2<sup>3</sup>\*2</sup>/<sub>2<sup>5</sup></sub>  
= 0.5  
I(X)=log<sub>2</sub>2=1  

* I  
I(X)=log<sub>2</sub><sup>26</sup>/<sub>23</sub>  

* J  
I(X)=log<sub>2</sub><sup>16</sup>/<sub>7</sub>  

## Two's Complement
num | answer
--- | ------
A | 101011
B | 0xCD
C | -42
D | 9 bits
E | Yes. 0xFA
F | No
G | 0xB3 -77
H | -128
I | 0x24 0x70
J | -16~15
K | -14

## Variable-length Encodings

### A
symbol | encoding | num
------ | -------- | ---
A | 0   | 1
B | 10  | 2
C | 110 | 3
D | 111 | 3

### B~E
#2 #3 #3 #1  

### F
log<sub>2</sub><sup>1</sup>/<sub>0.66</sub>  

### G
type | encoding
------ | --------
Slider    | 00
Fastball  | 01
Other     | 10
Curveball | 110
Change-up | 111

### H
major | encoding
----- | --------
 6-1  | 111
 6-2  | 0
 6-3  | 10
 6-7  | 110
 
 ### I
 (5)  
 
 ### J
 3  
 
 ### K
 I(X)=log<sub>2</sub><sup>1</sup>/<sub>0.29</sub>  
 
 ### L
 I don't know.  
 
 ### M
 Message | encoding
 ------- | --------
    M1   |   0
    M2   |  110
    M3   |  1110
    M4   |  1111
    M5   |   10
 
 the average number of bits = 1\*0.6+3\*0.08+4\*0.02+4\*0.01+2\*0.29=1.54 bits  
 
 ### N
  Grade | encoding
 ------- | --------
    A   |   00
    B   |   01
    C   |   10
    D   |   110
    F   |   111
    
 ### O
 D  
 
 ## Error Detection and Correction
 
 num | answer
 --- | ------
  A  |  1 0
  B  | 11011
  C  |  1 0
  D  |   1
  E  | yes no
  F  | 4 3 1
  G  |   2
  H  |  (4,4)
  I  |  (4,2)
  J  |  (1,1)
  K  |  (4,4)
 
 
 
