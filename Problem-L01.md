## Problem 1
num | answer
--- | ------
 A  | log<sub>2</sub><sup>8</sup>/<sub>5</sub>
 B  | log<sub>2</sub>52  log<sub>2</sub>48  0
 C  | 3 bits
 D  | 5 bits
 
## Problem 2
num | answer
--- | ------
 A  |  A
 B  | ABAEC
 C  |  A
 D  | Tree#1
 E  |  1
 F  | sum p<sub>i</sub><sup>1</sup>/<sub>p<sub>i</sub></sub> for 2<=i<=12, the result is 3.2744. 3274.4bits
 H  | ~~No~~ Yes, but we have to encode more than one sum at a time.
 
### G 
 num | encoding
 --- | --------
  2  |  01110
  3  |  0110
  4  |  1111
  5  |  000
  6  |  100
  7  |  110
  8  |  101
  9  |  001
  10 |  010
  11 |  1110
  12 |  01111
  
 the expect number of bits per sum is 3.306
 
 ## Problem 3
  num | encoding
  --- | --------
   A  | log<sub>2</sub><sup>1</sup>/<sub>0.15</sub>
  
 ### B
 The single-bit error detection requires the min Hamming distance is 2.  
 The single-bit error correction requires the min Hamming distance is 3.
 
 ### C
 letter | encoding
 :----: | -------
    E   |    0
    A   |   100
    I   |   101
    O   |   110
    U   |   111
    
 the average number of bits is 2.2 bits
 
## Problem 4
  num | answer
  --- | ------
   A  | 2<sup>32</sup>
   B  | 00000000 00000000 00000000 00000000
   B  | 01111111 11111111 11111111 11111111 2<sup>32</sup>-1
   B  | 10000000 00000000 00000000 00000000 -2<sup>32</sup>
   C  | 0x0000 0025 0xFFF8 0000 0xDEAD BEEF
   
## Problem 5
  num | answer 
  --- | :-----
   A  | (1)(3)
   B  | (1)(1,1) (2)correct (3)(2,2) (4)data correct
   C  | The two bits are in the same row or column and one for data and one for parity. 
   C additional | This can happen with two parity bit errors, one in each of therow and column check bits. 
   D  |  2 
   E  |  1 bit
   F  |  6

## Problem 6

### A
*Digit i in the binary expansion of a data bit index indicates whether the index should be included in the
calculation of pi. For example, the first data bit (which has index 3 = 00011) would be used in the parity
calculation for parity bits p0 and p1. Likewise, the sixth data bit (which has index 10 = 01010) would be
used in the parity calculation for parity bits p1 and p3. Since no data bit is assigned an index which is a
power of two, we guarantee that each data bit is used in the calculation of at least two different parity bits.*

### B
*We need to find the data index that appears in the calculation p0, p2 and p3 but not in the calculations for p1
and p4. Indicies 13 and 15 appear in p0, p2 and p3, but index 15 appears in the calculation for p1. So the
index of the data bit that failed is 13.
We can construct the index of the failing data bit directly from the parity calculations using ei = 1 if the pi
failed and ei = 0 if it didn't. So if p0, p2 and p3 failed, and the others didn't, the index is e4e3e2e1e0 =
01101 = 1310.*

### C
*If errors occur in two separate parity bits, this will be misinterpreted as a single data bit error. Also when
certain pairs of data bits have errors, the double-bit error masquerades as a single-bit error in another,
unrelated bit (e.g., suppose bits with indicies 19 and 21 both have errors).
We can detect these situations by adding an additional parity bit, p5, which is the parity of all other parity
and data bits. If a single data bit failed, this bit would indicate and error. But if exactly two bits have failed,
p5 would indicate no error, but p0, p1, ..., p4 would indicate the presence of some error (although the
indication might point at the wrong data bit). So, if by looking at p0, p1, ..., p4 it seems as though an error
occurred, we should check p5 to make sure that only one error occurred. If p5 does not indicate an error,
then a double-bit error occurred.*
