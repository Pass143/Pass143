- 👋 Hi, I’m @Pass143
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Pass143/Pass143 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#Lagrange Interpolation
#Importing NumPy Library
import numpy as np
# Reading number of unknowns
n = int(input('Enter number of data points: '))
# Making numpy array of n & n x n size and initializing
# to zero for storing x and y value along with differences of y
x = np.zeros((n))
y = np.zeros((n))
# Reading data points
print('Enter data for x and y: ')
for i in range(n):
x[i] = float(input( 'x['+str(i)+']='))
y[i] = float(input( 'y['+str(i)+']='))
# Reading interpolation point
xp = float(input('Enter interpolation point: '))
# Set interpolated value initially to zero
yp = 0
# Implementing Lagrange Interpolation
for i in range(n):
p = 1
for j in range(n):
if i != j:
p = p * (xp - x[j])/(x[i] - x[j])
yp = yp + p * y[i]
# Displaying output
print('Interpolated value at %.3f is %.3f.' % (xp, yp))
