### Exercise B: Spatial Operations (45 minutes)

1. **Convolution** (20 minutes)
Given the following 3×3 kernel:
```
[1][2][1]
[0][0][0]
[-1][-2][-1]
```
   - Apply this kernel to the center pixel of the following 5×5 image:
```
[100][100][100][100][100]
[100][150][150][150][100]
[100][150][200][150][100]
[100][150][150][150][100]
[100][100][100][100][100]
```
   - Show all steps of the calculation
   - What type of edge detection is this kernel performing?

2. **Edge Detection** (15 minutes)
   - Apply Sobel edge detection to this 3×3 image section:
```
[50][50][200]
[50][50][200]
[50][50][200]
```
   - Calculate both horizontal and vertical gradients
   - Calculate the magnitude
   - Determine if there's an edge (using threshold = 100)

3. **Median Filtering** (10 minutes)
   - Apply 3×3 median filtering to remove noise from:
```
[50][50][200]
[50][255][50]
[50][50][50]
```
   - Show the sorting process
   - What is the advantage of median filtering over mean filtering in this case?
