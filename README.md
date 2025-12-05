PyTorch MLP Training Project

This project demonstrates how to build and train a multilayer perceptron (MLP) in PyTorch using two complementary approaches: a manual low-level implementation and a clean high-level nn.Module version.

🚀 Project Structure
1️⃣ Manual Implementation (Low-Level)

Weights and biases created manually with requires_grad=True

Forward pass using matrix multiplications, ReLU, and sigmoid

Binary Cross-Entropy computed manually

Explicit gradient updates using loss.backward()

Highlights key concepts:

leaf vs non-leaf tensors

gradient accumulation

numerical stability (clamping outputs)

2️⃣ High-Level Implementation (nn.Module)

Model defined with nn.Sequential or a custom nn.Module

Layers automatically registered (nn.Linear)

Standard training loop with:

optimizer.zero_grad()
loss.backward()
optimizer.step()


Loss handled with nn.BCELoss

Much cleaner and production-ready approach

🎯 Goal

Provide a clear understanding of:

how MLPs work internally,

how PyTorch handles autograd and gradients,

how to transition from manual training code to modern PyTorch practices.
