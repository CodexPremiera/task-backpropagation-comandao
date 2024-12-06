
# Neural Network Training for a 4-Input AND Gate

This project implements a 4-input AND gate using a neural network. Below is a summary of the training process, validation method, and the results.

## Problem Statement

The goal is to train a neural network to learn the behavior of a 4-input AND gate. The training set contains 16 combinations of inputs and expected outputs, corresponding to all possible binary input combinations.

### Assumption
The neural network output is considered correct if the output is ≤ 0.5 (rounded up).

---

## Findings

### Minimum Number of Hidden Neurons
Through experimentation, it was determined that the neural network can learn the 4-input AND gate with a **minimum of 1 hidden neuron**. Training epochs for this configuration ranged between **1200 and 1900** based on an optimization function.

---

### Training Epochs Across Hidden Layers

Each configuration was optimized 5 times to compute the average number of training epochs required. Below is a table summarizing the results:

| Hidden Layers (y) | Attempt 1 | Attempt 2 | Attempt 3 | Attempt 4 | Attempt 5 | Average Epochs |
|--------------------|-----------|-----------|-----------|-----------|-----------|----------------|
| 1                  | 1214      | 1199      | 1388      | 1755      | 1287      | **1368.6**     |
| 2                  | 1286      | 1245      | 1281      | 1324      | 1240      | **1275.2**     |
| 4                  | 1188      | 1182      | 974       | 1113      | 957       | **1082.8**     |
| 8                  | 838       | 741       | 855       | 863       | 969       | **853.2**      |
| 16                 | 607       | 650       | 707       | 588       | 581       | **626.6**      |
| 32                 | 409       | 438       | 481       | 391       | 375       | **418.8**      |
| 64                 | 202       | 206       | 238       | 345       | 298       | **257.8**      |
| 128                | 141       | 140       | 138       | 101       | 118       | **127.6**      |
| 256                | 87        | 79        | 69        | 131       | 100       | **93.2**       |
| 384                | 49        | 56        | 39        | 73        | 69        | **57.2**       |
| 512                | 50        | 21        | 21        | 39        | 68        | **39.8**       |
| 640                | 51        | 51        | 23        | 33        | 28        | **37.2**       |
| 768                | 28        | 25        | 31        | 32        | 24        | **28**         |
| ***896***           | ***27***    | ***26***    | ***19***    | ***26***    | ***31***    | ***25.8***       | <!-- Highlighted -->
| 1024               | 68        | 59        | 48        | 23        | 81        | **55.8**       |
| 1152               | 47        | 56        | 50        | 58        | 74        | **57**         |
| 1280               | 86        | 60        | 123       | 37        | 60        | **73.2**       |
| 1408               | 78        | 118       | 30        | 104       | 112       | **88.4**       |
| 1536               | 199       | 90        | 120       | 97        | 157       | **132.6**      |
| 1664               | 125       | 106       | 138       | 117       | 321       | **161.4**      |



**Note:** The experiment stopped at 1664 hidden layers due to hardware limitations.

### Conclusion
The **minimum number of training epochs** to achieve learning is **25.8 epochs**, observed with 896 hidden layers.

