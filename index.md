# Content
[[python]]
[[thermodynamics]]

```python
import numpy as np
import matplotlib.pyplot as plt
import sympy as sp

def y(x):
    return x**2 + 3*x - 2

x = sp.symbols("x")
expr = x**2 + 3*x - 1
f = sp.lambdify(x, expr, "numpy")

xs = np.linspace(-1000,1000,1000)

plt.plot(x, y(x))
plt.plot(x, f(x))
plt.grid(True)
plt.show()
```
