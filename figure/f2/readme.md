

```bash

# Define the parabolic loss function with local minima
def parabolic_loss_with_dips(t):
    """
    Generate a parabolic loss function with five local minima at specific points.
    
    Parameters:
    t : numpy array
        Input array representing the variable.
    
    Returns:
    numpy array
        Loss function with local minima.
    """

    # t = t[0]
    # Base parabolic function
    base_parabola = (t / 10) ** 2
    
    # Add small dips at specified local minima
    dips = (
        0.1 * np.exp(-50 * (t - 9) ** 2) +
        0.1 * np.exp(-50 * (t - 8) ** 2) +
        0.1 * np.exp(-50 * (t - 7) ** 2) +
        0.1 * np.exp(-50 * (t - 6) ** 2) +
        0.1 * np.exp(-50 * (t - 5) ** 2) +
        0.1 * np.exp(-50 * (t - 4) ** 2) +

        0.1 * np.exp(-50 * (t + 9) ** 2) +
        0.1 * np.exp(-50 * (t + 8) ** 2) +
        0.1 * np.exp(-50 * (t + 7) ** 2) +
        0.1 * np.exp(-50 * (t + 6) ** 2) +
        0.1 * np.exp(-50 * (t + 5) ** 2) +
        0.1 * np.exp(-50 * (t + 4) ** 2) 

    )
    
    return base_parabola - dips

f = parabolic_loss_with_dips

```

![image](https://github.com/user-attachments/assets/23b99be2-c545-45f9-b8d4-2739abc90356)

