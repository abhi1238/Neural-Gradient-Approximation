# Parabolic Loss Function with Dips

## Overview
This function defines a **parabolic loss function with small valleys (dips)** in a **3D space**.

## Mathematical Formulation
The base function is a simple **paraboloid**:
\[
f(x, y) = x^2 + y^2
\]
To introduce local dips, we subtract Gaussian functions centered at specific points.

## Usage
```python
import numpy as np

def parabolic_loss_with_dips_3D(args):
    x, y = args
    base_parabola = x**2 + y**2
    
    dips = sum(
        10 * np.exp(-5 * ((x - i) ** 2 + (y - j) ** 2))
        for i in list(range(-5, -2)) + list(range(3, 6))  
        for j in list(range(-5, -2)) + list(range(3, 6))   
    )
    
    return base_parabola - dips
