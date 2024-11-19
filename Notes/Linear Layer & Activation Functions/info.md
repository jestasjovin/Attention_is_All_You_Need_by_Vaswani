### 1. **Linear Layers**
Linear layers are the simplest kind of neural network layer. They perform a linear transformation on their input.

**Math operation** 


y = W.x + b


Where:
-  y  is the output vector.
-  x  is the input vector.
-  W  is the weight matrix.
-  b  is the bias vector.



>>>
**SUMMARY**
eg in pytorch
- **in**: size of input vector.
- **out**: size of output vector.
- The `Linear` layer will learn the parameters  W  and  b  during training.

```python
linear_layer = nn.Linear(in_features=10, out_features=5)
```
- then you can use the layer to predict other values
```python
y = linear_layer(x)
```

>>>








---

### 2. **Activation Functions**

Activation functions introduce **non-linearity** into the model, by making it linear it won't be easy to judge for similar but with slight variation situations. 
>>>
Examples.

##### **ReLU (Rectified Linear Unit)** 
- It outputs 0 for negative input and returns the input value for positive input:

##### **Softmax**

**Softmax** It turns a vector of values into probabilities by exponentiating each element and then normalizing by dividing by the sum of all exponentiated values.
##### **Sigmoid**

The **Sigmoid** function squashes the input to a range between 0 and 1. It's used in binary classification problems or when the output needs to be interpreted as a probability for a single class:
>>>

### 3. **Layer Normalization**

**Layer Normalization** is a technique used to stabilize and accelerate training by normalizing the inputs to each layer. 




### Applications in a Transformer

- The **Multi-Head Attention**  uses linear layers to transform the input queries, keys, and values.
- After the attention operation, the results are passed through a **Layer Normalization** step.
- Then, a **Feedforward Network** (uses linear layers) is applied.
