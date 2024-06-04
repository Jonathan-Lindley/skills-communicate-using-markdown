# le H1 header
##### le H5 header
![Image of Les Paul guitar](https://th.bing.com/th/id/OIP.XZvMx2Je03DlMkuPH3DBIAHaHa?w=183&h=184&c=7&r=0&o=5&dpr=1.3&pid=1.7)
``` python
N = 4
def RLVs(N):
    reciprocal_vectors = []
    for h in range(-N, N + 1):
        for k in range(-N, N + 1):
            for l in range(-N, N + 1):
                # Check if all indices are either even or odd to obey structure factor rules
                if (h % 2 == 0 and k % 2 == 0 and l % 2 == 0) or \
                   (h % 2 != 0 and k % 2 != 0 and l % 2 != 0):
                    vec = (h, k, l)
                    magnitude = np.linalg.norm(vec)
                    reciprocal_vectors.append(vec)
    # Arrange reciprocal vectors in order of increaing magnitude
    reciprocal_vectors.sort(key=lambda vec: np.linalg.norm(vec))
    return reciprocal_vectors
```

- [x] thing that has been done
- [ ] thing that needs to be done
