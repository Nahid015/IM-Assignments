```python
#Nahid Hossain Taz- Assignment:1
#Upskill IM - 2021
import numpy as np
import matplotlib.pyplot as plt

# Stylesheets defined in Matplotlib - Here I use 'ggplot'
plt.style.use('ggplot')

# Set up runtime comparison points for n=7
n=7
k = 4
x = np.linspace(1, n, num= 1000)
labels = [ 'Logarithmic', 'Linear', 'Quadratic', 'Cubic', 'Polynomial']
big_o_notation = [ np.log2(x), x, x**2, x**3, x**k]

# Plot setup
plt.figure(figsize=(15, 10))
plt.xlim(0, 7)
plt.ylim(0, 15)

for i in range(len(big_o_notation)):
    plt.plot(x, big_o_notation[i], label=labels[i])

plt.legend(loc=0)
plt.ylabel('Relative Runtime')
plt.xlabel('Input Size')
plt.savefig('big-o-notation.png')

```


![png](output_0_0.png)

