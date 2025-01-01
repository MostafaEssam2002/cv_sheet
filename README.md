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
1. **Convolution** (20 minutes)


#### **Kernel**:
\[
\begin{bmatrix}
1 & 2 & 1 \\
0 & 0 & 0 \\
-1 & -2 & -1
\end{bmatrix}
\]

#### **Image**:
\[
\begin{bmatrix}
100 & 100 & 100 & 100 & 100 \\
100 & 150 & 150 & 150 & 100 \\
100 & 150 & 200 & 150 & 100 \\
100 & 150 & 150 & 150 & 100 \\
100 & 100 & 100 & 100 & 100
\end{bmatrix}
\]

---

### **2. Convolution Process**

#### **Center Pixel**:
The center pixel is \(200\) (at position \((2, 2)\)) in the 5×5 image. The 3×3 region around it is:

\[
\begin{bmatrix}
150 & 150 & 150 \\
150 & 200 & 150 \\
150 & 150 & 150
\end{bmatrix}
\]


---

### **Step-by-Step Calculation**
We multiply each value in the 3×3 region with the corresponding value in the kernel and sum the results.

1. **Top Row**:
   - (1 X 150) + (2 X 150) + (1 X 150) = 150 + 300 + 150 = 600

2. **Middle Row**:
   - (0 X 150) + (0 X 200) + (0 X 150) = 0

3. **Bottom Row**:
   - (-1 X 150) + (-2 X 150) + (-1 X 150) = -150 - 300 - 150 = -600

4. **Sum of All Rows**:
   \[
   600 + 0 - 600 = 0
   \]

---

### **3. Final Result**
The result of the convolution at the center pixel is **0**.

---

### **4. Edge Detection Type**
This kernel is the **Sobel Operator** in the **vertical direction**, designed to detect vertical edges in an image. Specifically:
- High positive values indicate light-to-dark transitions in the vertical direction.
- High negative values indicate dark-to-light transitions in the vertical direction.
- A result of \(0\) indicates no vertical edge at the center pixel.
