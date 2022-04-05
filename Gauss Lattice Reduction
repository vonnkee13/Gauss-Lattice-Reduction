import numpy as np
import matplotlib.pyplot as plt
def GLR(v1,v2): #v1,v2 are the input basis vectors of a 2-dim'l lattice
    v1 = vector(v1)
    v2 = vector(v2)
    while True:
        if norm(v2)<norm(v1): #we want v1 to be the shorter vector
            v1, v2 = v2, v1
        m = round(v1.dot_product(v2)/norm(v1)^2)
        if m == 0:
            print("The shortest vector is",v1)
            print("The other reduced basis vector is",v2)
            break
        v2 = v2 - m*v1
        V = np.array([v1,v2])
        origin = np.array([[0, 0],[0, 0]]) # origin point
        plt.quiver(*origin, V[:,0], V[:,1], color=['r','b','g'], scale=round(norm(v1)))
        plt.show()
