import numpy as np

# Define a 3x4 augmented matrix
# Each row: [a, b, c, d] → ax + by + cz = d
matrix = np.array([
    [2, 3, -1, 5],
    [-1, 7, 2, 10],
    [3, -2, 4, 1]
])

# Separate A (coefficients) and b (constants)
A = matrix[:, :3]
b = matrix[:, 3]

# Solve the system
try:
    solution = np.linalg.solve(A, b)
    print("solution (x, y, z):")
    print(solution)
except np.linalg.LinAlgError:
    print("The system cannot be solved (singular matrix or infinite solutions".)
