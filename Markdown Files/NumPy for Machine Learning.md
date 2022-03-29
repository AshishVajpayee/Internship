### NumPy for Machine Learning
- `Numerical analysis` with the NumPy computing package.


### Set up
- First we'll import the `NumPy` package and set seeds for reproducibility so that we can receive the exact same results every time.


```python
import numpy as np
```


```python
# Set seed for reproducibility
np.random.seed(seed=1234)
```

#### Basics 
- Scalar (0D tensor) single value
- Vector (1D tensor) row or column of values
- Matrix (2D tensor) array(rows and columns of values)
- 3D tensor, etc


```python
# Scalar
x = np.array(6)
print ("x: ", x)
print ("x ndim: ", x.ndim) # number of dimensions
print ("x shape:", x.shape) # dimensions
print ("x size: ", x.size) # size of elements
print ("x dtype: ", x.dtype) # data type
```

    x:  6
    x ndim:  0
    x shape: ()
    x size:  1
    x dtype:  int32
    


```python
# Vector
x = np.array([1.3 , 2.2 , 1.7])
print ("x: ", x)
print ("x ndim: ", x.ndim)
print ("x shape:", x.shape)
print ("x size: ", x.size)
print ("x dtype: ", x.dtype) # notice the float datatype
```

    x:  [1.3 2.2 1.7]
    x ndim:  1
    x shape: (3,)
    x size:  3
    x dtype:  float64
    


```python
# Matrix
x = np.array([[1,2], [3,4]])
print ("x:\n", x)
print ("x ndim: ", x.ndim)
print ("x shape:", x.shape)
print ("x size: ", x.size)
print ("x dtype: ", x.dtype)
```

    x:
     [[1 2]
     [3 4]]
    x ndim:  2
    x shape: (2, 2)
    x size:  4
    x dtype:  int32
    


```python
# 3-D Tensor
x = np.array([[[1,2],[3,4]],[[5,6],[7,8]]])
print ("x:\n", x)
print ("x ndim: ", x.ndim)
print ("x shape:", x.shape)
print ("x size: ", x.size)
print ("x dtype: ", x.dtype)
```

    x:
     [[[1 2]
      [3 4]]
    
     [[5 6]
      [7 8]]]
    x ndim:  3
    x shape: (2, 2, 2)
    x size:  8
    x dtype:  int32
    

<p>NumPy also comes with several functions that allow us to create tensors quickly.</p>


```python
# Functions
print ("np.zeros((2,2)):\n", np.zeros((2,2))) # prints 2, 2 matrix with 0's
print ("np.ones((2,2)):\n", np.ones((2,2))) # prints 2, 2 matrix with 1's
print ("np.eye((2)):\n", np.eye((2))) # identity matrix
print ("np.random.random((2,2)):\n", np.random.random((2,2))) # prints random 2,2 matrix with random values
```

    np.zeros((2,2)):
     [[0. 0.]
     [0. 0.]]
    np.ones((2,2)):
     [[1. 1.]
     [1. 1.]]
    np.eye((2)):
     [[1. 0.]
     [0. 1.]]
    np.random.random((2,2)):
     [[0.77997581 0.27259261]
     [0.27646426 0.80187218]]
    

### Indexing
- We can extract specific values from our tensors using indexing.

- Keep in mind that when indexing the row and column, indices start at 0. And like indexing with lists, we can use negative indices as well (where -1 is the last item).


```python
# Indexing
x = np.array([1, 2, 3])
print ("x: ", x)
print ("x[0]: ", x[0])
x[0] = 0
print ("x: ", x)
```

    x:  [1 2 3]
    x[0]:  1
    x:  [0 2 3]
    


```python
# Slicing
x = np.array([[1,2,3,4], [5,6,7,8], [9,10,11,12]])
print (x)
print ("x column 1: ", x[:, 1]) # prints the values of column 1
print ("x row 0: ", x[0, :])  # prints the values of row 0
print ("x rows 0,1 & cols 1,2: \n", x[0:2, 1:3]) # little confusing
```

    [[ 1  2  3  4]
     [ 5  6  7  8]
     [ 9 10 11 12]]
    x column 1:  [ 2  6 10]
    x row 0:  [1 2 3 4]
    x rows 0,1 & cols 1,2: 
     [[2 3]
     [6 7]]
    


```python
# Integer array indexing
print (x)
rows_to_get = np.array([0, 1, 2])
print ("rows_to_get: ", rows_to_get)
cols_to_get = np.array([0, 2, 1])
print ("cols_to_get: ", cols_to_get)
# Combine sequences above to get values to get
print ("indexed values: ", x[rows_to_get, cols_to_get]) # (0, 0), (1, 2), (2, 1)
```

    [[ 1  2  3  4]
     [ 5  6  7  8]
     [ 9 10 11 12]]
    rows_to_get:  [0 1 2]
    cols_to_get:  [0 2 1]
    indexed values:  [ 1  7 10]
    


```python
# Boolean array indexing
x = np.array([[1, 2], [3, 4], [5, 6]])
print ("x:\n", x)
print ("x > 2:\n", x > 2)
print ("x[x > 2]:\n", x[x > 2])
```

    x:
     [[1 2]
     [3 4]
     [5 6]]
    x > 2:
     [[False False]
     [ True  True]
     [ True  True]]
    x[x > 2]:
     [3 4 5 6]
    

### Arithmetic


```python
# Basic math
x = np.array([[1,2], [3,4]], dtype=np.float64)
y = np.array([[1,2], [3,4]], dtype=np.float64)
print ("x + y:\n", np.add(x, y)) # or x + y example (1 + 1), (2 + 2) = [2. 4.]
print ("x - y:\n", np.subtract(x, y)) # or x - y
print ("x * y:\n", np.multiply(x, y)) # or x * y
```

    x + y:
     [[2. 4.]
     [6. 8.]]
    x - y:
     [[0. 0.]
     [0. 0.]]
    x * y:
     [[ 1.  4.]
     [ 9. 16.]]
    

### Dot product
One of the most common NumPy operations we’ll use in machine learning is matrix multiplication using the dot product. Suppose we wanted to take the dot product of two matrices with shapes `[2 X 3]` and `[3 X 2]`. We take the rows of our first matrix (2) and the columns of our second matrix (2) to determine the dot product, giving us an output of `[2 X 2]`. The only requirement is that the inside dimensions match, in this case the first matrix has 3 columns and the second matrix has 3 rows.


```python
# Dot product
a = np.array([[1,2,3], [4,5,6]], dtype=np.float64) # we can specify dtype
b = np.array([[7,8], [9,10], [11, 12]], dtype=np.float64)
c = a.dot(b)
print (f"{a.shape} · {b.shape} = {c.shape}")
print (c)
```

    (2, 3) · (3, 2) = (2, 2)
    [[ 58.  64.]
     [139. 154.]]
    

### Axis operations
We can also do operations across a specific axis


```python
# Sum across a dimension
x = np.array([[1,2],[3,4]])
print (x)
print ("sum all: ", np.sum(x)) # adds all elements 1+2+3+4 = 10
print ("sum axis=0: ", np.sum(x, axis=0)) # sum across rows 1+3 = 4, 2+4 = 6
print ("sum axis=1: ", np.sum(x, axis=1)) # sum across columns 1+2 = 3, 2+4=7
```

    [[1 2]
     [3 4]]
    sum all:  10
    sum axis=0:  [4 6]
    sum axis=1:  [3 7]
    

### Broadcast
What happens when we try to do operations with tensors with seemingly incompatible shapes? Their dimensions aren’t compatible as is but how does NumPy still gives us the right result? This is where broadcasting comes in. The scalar is broadcast across the vector so that they have compatible shapes.


```python
# Broadcasting
x = np.array([1,2]) # vector
y = np.array(3) # scalar
z = x + y
print ("z:\n", z)
```

    z:
     [4 5]
    

### Gotchas
- In the situation below, what is the value of **`c`** and what are its dimensions?


```python
a = np.array((3, 4, 5))
b = np.expand_dims(a, axis=1)
c = a + b
```


```python
a.shape # (3,)
b.shape # (3, 1)
c.shape # (3, 3)
print (c)
```

    [[ 6  7  8]
     [ 7  8  9]
     [ 8  9 10]]
    

### Transpose
We often need to change the dimensions of our tensors for operations like the dot product. If we need to switch two dimensions, we can transpose the tensor.


```python
# Transposing
x = np.array([[1,2,3], [4,5,6]])
print ("x:\n", x)
print ("x.shape: ", x.shape)
y = np.transpose(x, (1,0)) # flip dimensions at index 0 and 1
print ("y:\n", y)
print ("y.shape: ", y.shape)
```

    x:
     [[1 2 3]
     [4 5 6]]
    x.shape:  (2, 3)
    y:
     [[1 4]
     [2 5]
     [3 6]]
    y.shape:  (3, 2)
    

### Reshape
Sometimes, we'll need to alter the dimensions of the matrix. Reshaping allows us to transform a tensor into different permissible shapes. Below, our reshaped tensor has the same number of values as the original tensor. (`1X6` = `2X3`). We can also use `-1` on a dimension and `NumPy` will infer the dimension based on our input tensor.



```python
# Reshaping
x = np.array([[1,2,3,4,5,6]])
print (x)
print ("x.shape: ", x.shape)

y = np.reshape(x, (2, 3)) # reshapes 2 x 3 matrix
print ("y: \n", y)
print ("y.shape: ", y.shape) 

z = np.reshape(x, (2, -1)) # -1 takes last value i.e, 3
print ("z: \n", z)
print ("z.shape: ", z.shape)
```

    [[1 2 3 4 5 6]]
    x.shape:  (1, 6)
    y: 
     [[1 2 3]
     [4 5 6]]
    y.shape:  (2, 3)
    z: 
     [[1 2 3]
     [4 5 6]]
    z.shape:  (2, 3)
    

### Joining
We can also join our tensors via [concatentation](https://numpy.org/doc/stable/reference/generated/numpy.concatenate.html) or [stacking](https://numpy.org/doc/stable/reference/generated/numpy.stack.html) .


```python
x = np.random.random((2, 3))
print (x)
print (x.shape)
```

    [[0.95813935 0.87593263 0.35781727]
     [0.50099513 0.68346294 0.71270203]]
    (2, 3)
    


```python
# Concatenation
y = np.concatenate([x, x], axis=0) # concat on a specified axis
print (y)
print (y.shape)
```

    [[0.95813935 0.87593263 0.35781727]
     [0.50099513 0.68346294 0.71270203]
     [0.95813935 0.87593263 0.35781727]
     [0.50099513 0.68346294 0.71270203]]
    (4, 3)
    


```python
# Stacking
z = np.stack([x, x], axis=0) # stack on new axis
print (z)
print (z.shape)
```

    [[[0.95813935 0.87593263 0.35781727]
      [0.50099513 0.68346294 0.71270203]]
    
     [[0.95813935 0.87593263 0.35781727]
      [0.50099513 0.68346294 0.71270203]]]
    (2, 2, 3)
    

### Expanding / reducing
We can also easily add and remove dimensions to our tensors and we'll want to do this to make tensors compatible for certain operations.


```python
# Adding dimensions
x = np.array([[1,2,3],[4,5,6]]) # 2x3 matrix
print ("x:\n", x)
print ("x.shape: ", x.shape)
y = np.expand_dims(x, 1) # expand dim 1
print ("y: \n", y)
print ("y.shape: ", y.shape)   # notice extra set of brackets are added
```

    x:
     [[1 2 3]
     [4 5 6]]
    x.shape:  (2, 3)
    y: 
     [[[1 2 3]]
    
     [[4 5 6]]]
    y.shape:  (2, 1, 3)
    


```python
# Removing dimensions
x = np.array([[[1,2,3]],[[4,5,6]]])
print ("x:\n", x)
print ("x.shape: ", x.shape)
y = np.squeeze(x, 1) # squeeze dim 1
print ("y: \n", y)
print ("y.shape: ", y.shape)  # notice extra set of brackets are gone
```

    x:
     [[[1 2 3]]
    
     [[4 5 6]]]
    x.shape:  (2, 1, 3)
    y: 
     [[1 2 3]
     [4 5 6]]
    y.shape:  (2, 3)
    
