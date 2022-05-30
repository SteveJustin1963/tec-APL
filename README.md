# tec-APL
APL extensions written in Forth/MINT for the TEC1

### https://en.wikipedia.org/wiki/APL_syntax_and_symbols
### Monadic functions 

|Name(s)|Notation|Meaning|Unicode code point|MINT|
|-------|----|----|----|----|
|Roll|	?B|	One integer selected randomly from the first B integers	U+003F ?
|Ceiling	⌈B	Least integer greater than or equal to B	U+2308 ⌈
|Floor	⌊B	Greatest integer less than or equal to B	U+230A ⌊
|Shape, Rho	⍴B	Number of components in each dimension of B	U+2374 ⍴
|Not, Tilde	∼B	Logical: ∼1 is 0, ∼0 is 1	U+223C ∼
|Absolute value	∣B	Magnitude of B	U+2223 ∣
|Index generator, Iota	⍳B	Vector of the first B integers	U+2373 ⍳
|Exponential	⋆B	e to the B power	U+22C6 ⋆
|Negation	−B	Changes sign of B	U+2212 −
|Conjugate	+B	The complex conjugate of B (real numbers are returned unchanged)	U+002B +
|Signum	×B	¯1 if B<0; 0 if B=0; 1 if B>0	U+00D7 ×
|Reciprocal	÷B	1 divided by B	U+00F7 ÷
|Ravel, Catenate, Laminate	,B	Reshapes B into a vector	U+002C ,
|Matrix inverse, Monadic Quad Divide	⌹B	Inverse of matrix B	U+2339 ⌹
|Pi times	○B	Multiply by π	U+25CB ○
|Logarithm	⍟B	Natural logarithm of B	U+235F ⍟
|Reversal	⌽B	Reverse elements of B along last axis	U+233D ⌽
|Reversal	⊖B	Reverse elements of B along first axis	U+2296 ⊖
|Grade up	⍋B	Indices of B which will arrange B in ascending order	U+234B ⍋
|Grade down	⍒B	Indices of B which will arrange B in descending order	U+2352 ⍒
|Execute	⍎B	Execute an APL expression	U+234E ⍎
|Monadic format	⍕B	A character representation of B	U+2355 ⍕
|Monadic transpose	⍉B	Reverse the axes of B	U+2349 ⍉
|Factorial	!B	Product of integers 1 to B	U+0021 !
 

### Dyadic functions


|Name(s)|Notation|Meaning|Unicode code point|MINT|
|-------|----|----|----|----|
|Add| A+B| Sum of A and B| U+002B +|
|Subtract| A−B| A minus B| U+2212 −|
|Multiply| A×B| A multiplied by B| U+00D7 ×|
|Divide| A÷B| A divided by B| U+00F7 ÷|
|Exponentiation| A⋆B| A raised to the B power| U+22C6 ⋆|
|Circle| A○B| Trigonometric functions of B selected by A|
|||A=1: sin(B)    A=5: sinh(B)|
|||A=2: cos(B)    A=6: cosh(B)|
|||A=3: tan(B)    A=7: tanh(B)|
|||Negatives produce the inverse of the respective functions |U+25CB ○|
|Deal| A?B| A distinct integers selected randomly from the first B integers| U+003F ?|
|Membership, Epsilon| A∈B| 1 for elements of A present in B; 0 where not.| U+2208 ∈|
|Find, Epsilon Underbar| A⍷B| 1 for starting point of multi-item array A present in B; 0 where not.| U+2377 ⍷|
|Maximum, Ceiling| A⌈B| The greater value of A or B| U+2308 ⌈|
|Minimum, Floor| A⌊B| The smaller value of A or B| U+230A ⌊|
|Reshape, Dyadic Rho| A⍴B| Array of shape A with data B| U+2374 ⍴|
|Take| A↑B| Select the first (or last) A elements of B according to ×A| U+2191 ↑|
|Drop| A↓B| Remove the first (or last) A elements of B according to ×A| U+2193 ↓|
|Decode| A⊥B| Value of a polynomial whose coefficients are B at A| U+22A5 ⊥|
|Encode| A⊤B| Base-A representation of the value of B| U+22A4 ⊤|
|Residue| A∣B| B modulo A| U+2223 ∣|
|Catenation| A,B| Elements of B appended to the elements of A| U+002C ,|
|Expansion, Dyadic Backslash| A\B| Insert zeros (or blanks) in B corresponding to zeros in A| U+005C \|
|Compression, Dyadic Slash| A/B| Select elements in B corresponding to ones in A| U+002F /|
|Index of, Dyadic Iota| A⍳B| The location (index) of B in A; 1+⍴A if not found| U+2373 ⍳|
|Matrix divide, Dyadic Quad Divide| A⌹B| Solution to system of linear equations, multiple regression Ax = B| U+2339 ⌹|
|Rotation| A⌽B| The elements of B are rotated A positions| U+233D ⌽|
|Rotation| A⊖B| The elements of B are rotated A positions along the first axis| U+2296 ⊖|
|Logarithm| A⍟B| Logarithm of B to base A| U+235F ⍟|
|Dyadic format| A⍕B| Format B into a character matrix according to A| U+2355 ⍕|
|General transpose| A⍉B| The axes of B are ordered by A| U+2349 ⍉|
|Combinations| A!B| Number of combinations of B taken A at a time| U+0021 !|
|Diaeresis, Dieresis, Double-Dot| A¨B| Over each, or perform each separately; B = on these; A = operation to perform or using (e.g., iota)| U+00A8 ¨|
|Less than| A<B| Comparison: 1 if true, 0 if false| U+003C <|
|Less than or equal| A≤B| Comparison: 1 if true, 0 if false| U+2264 ≤|
|Equal| A=B| Comparison: 1 if true, 0 if false| U+003D =|
|Greater than or equal| A≥B| Comparison: 1 if true, 0 if false| U+2265 ≥|
|Greater than| A>B| Comparison: 1 if true, 0 if false| U+003E >|
|Not equal| A≠B| Comparison: 1 if true, 0 if false| U+2260 ≠|
|Or| A∨B| Boolean Logic: 0 (False) if both A and B = 0, 1 otherwise. Alt: 1 (True) if A or B = 1 (True)| U+2228 ∨|
|And| A∧B| Boolean Logic: 1 (True) if both A and B = 1, 0 (False) otherwise| U+2227 ∧|
|Nor| A⍱B| Boolean Logic: 1 if both A and B are 0, otherwise 0. Alt: ~∨ = not Or| U+2371 ⍱|
|Nand| A⍲B| Boolean Logic: 0 if both A and B are 1, otherwise 1. Alt: ~∧ = not And| U+2372 ⍲|
|Left| A⊣B| A| U+22A3 ⊣|
|Right| A⊢B| B| U+22A2 ⊢|





### Ref
- https://www.gnu.org/software/apl/apl.html
- https://en.wikipedia.org/wiki/APL_syntax_and_symbols

