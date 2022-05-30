# tec-APL
APL extensions written in Forth/MINT for the TEC1


### Monadic functions https://en.wikipedia.org/wiki/APL_syntax_and_symbols#Monadic_and_dyadic_functions

|Name(s)|Notation|Meaning|Unicode code point|MINT|
|----|----|----|----|----|----|
Roll| ?B| One integer selected randomly from the first B integers| U+003F ?
Signum| ×B| ¯1 if B<0; 0 if B=0; 1 if B>0| U+00D7 ×
Reciprocal| ÷B| 1 divided by B| U+00F7 ÷
Conjugate| +B| The complex conjugate of B (real numbers are returned unchanged)| U+002B +
Ravel, Catenate, Laminate| ,B| Reshapes B into a vector| U+002C ,
Factorial| !B| Product of integers 1 to B| U+0021 !
Exponential| ⋆B| e to the B power| U+22C6 ⋆
Pi times| ○B| Multiply by π| U+25CB ○
Not, Tilde| ∼B| Logical: ∼1 is 0, ∼0 is 1| U+223C ∼
Floor| ⌊B| Greatest integer less than or equal to B| U+230A ⌊
Reversal| ⌽B| Reverse elements of B along last axis| U+233D ⌽
Grade up| ⍋B| Indices of B which will arrange B in ascending order| U+234B ⍋
Execute| ⍎B| Execute an APL expression| U+234E ⍎
Logarithm| ⍟B| Natural logarithm of B| U+235F ⍟
Negation| −B| Changes sign of B| U+2212 −
Absolute value| ∣B| Magnitude of B| U+2223 ∣
Reversal| ⊖B| Reverse elements of B along first axis| U+2296 ⊖
Ceiling| ⌈B| Least integer greater than or equal to B| U+2308 ⌈
Matrix inverse, Monadic Quad Divide| ⌹B| Inverse of matrix B| U+2339 ⌹
Monadic transpose| ⍉B| Reverse the axes of B| U+2349 ⍉
Grade down| ⍒B| Indices of B which will arrange B in descending order| U+2352 ⍒
Monadic format| ⍕B| A character representation of B| U+2355 ⍕
Index generator, Iota| ⍳B| Vector of the first B integers| U+2373 ⍳
Shape, Rho| ⍴B| Number of components in each dimension of B| U+2374 ⍴



### Dyadic functions





### Ref
- https://www.gnu.org/software/apl/apl.html
- https://en.wikipedia.org/wiki/APL_syntax_and_symbols

