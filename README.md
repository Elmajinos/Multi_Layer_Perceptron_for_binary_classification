🧠✨ PyTorch MLP Training Project

This project demonstrates how to build and train a multilayer perceptron (MLP) in PyTorch using both a manual low-level approach and a clean high-level nn.Module implementation.

🚀 Features

🔧 Manual weight initialization and updates

🧮 Forward pass with ReLU & Sigmoid

📉 Binary classification using BCE

🔁 Backpropagation with loss.backward()

⚙️ PyTorch autograd: leaf vs non-leaf tensors

🤖 High-level architecture using nn.Module

📊 Training loss visualization

📂 Project Structure
manual_mlp.py       # Manual implementation with explicit gradient updates
module_mlp.py       # High-level MLP using nn.Module
train.py            # Training loop and loss plotting

🏗️ Manual MLP (Low-Level)

This version shows how neural networks work internally:

🎯 Weights created with requires_grad=True

🧠 Forward propagation built manually using:

torch.mm()

F.relu()

torch.sigmoid()

🧾 BCE loss computed manually

🟡 Gradients computed with Autograd

🔧 Manual weight update:

W -= lr * W.grad


This highlights key PyTorch mechanics such as gradient flow, accumulation, and numerical stability.

🧱 High-Level MLP (nn.Module)

A cleaner and more scalable implementation:

class MyModel(nn.Module):
    def __init__(self):
        super().__init__()
        self.fc1 = nn.Linear(n_in, n_h1)
        self.fc2 = nn.Linear(n_h1, n_h2)
        self.fc3 = nn.Linear(n_h2, n_out)


Training follows the standard PyTorch loop:

optimizer.zero_grad()
loss.backward()
optimizer.step()


✔️ Shorter
✔️ More stable
✔️ Easier to extend
