# Liquid Time Constant - Recurrent Neural Network (LTC-RNN)

## Project Overview
This project implements a **Liquid Time-Constant Recurrent Neural Network (LTCRNN)**, which is a biologically-inspired neural network designed to model **dynamical systems**. It draws inspiration from **spiking neural networks** and **liquid neural networks**, using leaky integrate-and-fire (LIF) neuron dynamics to process temporal data.

---

## 1. Problem Statement
The model is used to learn and predict **non-linear trajectories**, demonstrated here through a **2D spiral dataset**. The primary goal is to:
- Capture temporal dependencies in sequential data.
- Predict the next position in the sequence based on past inputs.

---

## 2. Inputs and Outputs
**Input:**
- A sequence of 2D coordinates representing points on a spiral.

**Output:**
- Predicted 2D coordinates for the next point in the sequence.

**Expectation:**
- The model should approximate the trajectory of the spiral, learning the temporal relationships to generate outputs matching the target path.

---

## 3. Algorithms and Techniques
The model integrates:
1. **Liquid Neural Networks Concepts** - Inspired by continuous-time dynamical systems.
2. **LIF Neuron Dynamics** - Implements leaky integrate-and-fire (LIF) equations to simulate neuron behavior.
3. **ODE Solver Approximations** - Solves neuron dynamics iteratively for temporal updates.
4. **Stochastic Connectivity (Random Wiring)** - Generates random neuron connectivity to model a liquid neural network structure.
5. **Gradient Descent Optimization** - Backpropagation using Adam optimizer for weight updates.

---

## 4. Architecture
### Components:
1. **Random Wiring:**
   - Defines connectivity and weights between neurons.
   - Generates random adjacency matrices for sensory and internal connections.

2. **LIFNeuronLayer:**
   - Models neuron dynamics with LIF equations.
   - Processes input signals and updates neuron states.

3. **LTCCell:**
   - Encapsulates neuron behavior and updates states based on inputs.

4. **LTCRNN:**
   - Recurrent neural network wrapping the LIF dynamics.
   - Handles sequential data processing over time steps.

---

## 5. Computational Process
1. Generate a spiral dataset for trajectory prediction.
2. Preprocess data into input-output pairs for training.
3. Initialize model parameters and random wiring.
4. Train the network using **Mean Squared Error (MSE)** loss.
5. Perform **gradient updates** with the **Adam optimizer**.
6. Evaluate predictions by visualizing predicted and true paths.

---

## 6. Comparison and Evaluation
- The model does **not directly compare** with other methods in this implementation.
- Instead, performance is visually and numerically assessed by how well predictions follow the spiral trajectory.
- While computationally **intensive** due to iterative ODE solutions, this approach offers **greater flexibility** in modeling continuous-time processes than traditional RNNs or LSTMs.

---

## 7. Is This Reinforcement Learning?
No, this is **not a reinforcement learning problem**. Instead:
- It is a **sequence prediction task** based on supervised learning.
- Loss is minimized directly by comparing outputs to targets.

---

## 8. Advantages and Limitations
**Advantages:**
- Models continuous-time dynamics, enabling complex temporal pattern recognition.
- Biologically inspired design provides robustness to noise and dynamic changes.

**Limitations:**
- Computational cost is higher than standard RNNs.
- Requires tuning for hyperparameters like time constants and neuron connections.

---

## 9. References
1. "Liquid Time-Constant Networks" - Hasani, R., et al.
2. Biological neuron modeling concepts.

---

## 10. Future Work
- Extend the model to 3D trajectories.
- Incorporate feedback connections for closed-loop control.
- Optimize computational efficiency using GPU acceleration.


