
# Visualize the function

```bash
def parabolic_loss_with_dips_3D(args):
    x, y = args
    base_parabola = x**2 + y**2
    
    dips = sum(
        10 * np.exp(-5 * ((x - i) ** 2 + (y - j) ** 2))
        for i in list(range(-5, -2)) + list(range(3, 6))  
        for j in list(range(-5, -2)) + list(range(3, 6))   
    )
    
    return base_parabola - dips


f = parabolic_loss_with_dips_3D

```

![image](https://github.com/user-attachments/assets/7b8c38ff-3cec-44ed-8e7d-0d076fe14e69)
