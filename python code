import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data = pd.read_csv("data.csv")
phi = data['phi']
k = data['k (md)']
plt.figure(figsize=(10, 6))
plt.semilogy(phi, k, 'bo', markersize=5)

# Adding diagonal lines for different zones
x = np.linspace(min(phi), max(phi), 100)
for factor in [0.01, 0.1, 1, 10, 100, 1000, 10000]:
    y = factor * x
    plt.semilogy(x, y, '--', label=f'Zone {factor}')

plt.title("Porosity vs Permeability Curve")
plt.xlabel("Porosity")
plt.ylabel("Permeaility")

plt.grid(True, which='both', linestyle='--', linewidth=0.5)
plt.show()
