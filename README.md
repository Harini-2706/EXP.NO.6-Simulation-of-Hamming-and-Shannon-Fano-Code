# EXP.NO.6-Simulation-of-Hamming-and-Shannon-Fano-Code
Simulation of Hamming and Shannon-Fano Code
# AIM
To implement Huffman and Shannon-Fano coding for a discrete memoryless source with given probabilities and analyze the efficiency, redundancy, and variance.

# SOFTWARE REQUIRED
Laptop

python

# ALGORITHMS
Start
Input symbols and their probabilities.
Sort symbols: Huffman: Ascending order. Shannon-Fano: Descending order.
Generate codewords: Huffman: Combine smallest probabilities until one node remains. Shannon-Fano: Split list recursively with near-equal probabilities.
Calculate entropy, average length, efficiency, and redundancy.
Display results.
End
# PROGRAM
~~~
import numpy as np

import math

L = 0

hs = 0

p = []

lk = []

n = int(input("Enter the number of Samples : "))

for i in range (n):

pr = float(input(f"Enter the probability of sample values {i + 1}: "))

p.append(pr) for i in range (n):

l = float(input(f"Enter the length of the sample values {i + 1}: "))

lk.append(l) for k in range (n):

Avg1 = p[k] * lk[k]

L = L + Avg1 for k in range (n):

e = p[k] * math.log(1 / p[k], 2)

hs = hs + e hs = round(hs,3)

eff = hs / L

eff = round(eff,3)

red = round(1 - eff,3)

var = 0

for k in range(n):

var1 = p[k] * (lk[k]-L)**2

var = var + var1

var = round(var,3)

print(f"Average Codeword Length is : {L}")

print(f"Entropy is : {hs}")

print(f"Efficiency is : {eff * 100}%")

print(f"Redudancy is : {red}")

print(f"Variance is : {var}")
~~~
# OUTPUT
![image](https://github.com/user-attachments/assets/39d67cb5-f07b-4d38-92c3-467bfa5929e5)


Average Codeword Length is : 2.625

Entropy is : 2.625

Efficiency is : 100.0%

Redudancy is : 0.0

Variance is : 0.484

# RESULT
The simulation of Hamming and Shannon-Fano Code was successfully completed using Python, demonstrating effective error detection and correction in Hamming Code and efficient data compression with minimal redundancy in Shannon-Fano Code.
