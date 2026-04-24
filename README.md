Self-Pruning Neural Network
AI Engineer Case Study Submission

Ramanan G
AI Engineer · Deep Learning Enthusiast · Builder

Student Details
Field	Details
Full Name	Ramanan G
Roll Number	22MIA1150
Programme	M.Tech Integrated CSE with Business Analytics
CGPA	7.60 / 10.00
Status	Active Student
Project Overview

This project explores the concept of self-pruning neural networks, where the model learns to remove unnecessary weights during training rather than relying on post-training pruning.

A custom neural architecture is built using a PrunableLinear layer, where each weight is controlled by a learnable sigmoid gate. These gates are optimized jointly with model weights using an L1 sparsity regularization loss, encouraging the network to progressively suppress less important connections.

The model is trained on the CIFAR-10 dataset, and multiple experiments were conducted to analyze the accuracy–sparsity trade-off.

Key Components
PrunableLinear Layer
Introduces learnable gate parameters per weight
Uses sigmoid activation to softly mask weights
Self-Pruning MLP Architecture
Multi-layer perceptron with 4 prunable layers
Batch Normalization, ReLU, and Dropout for stability
Sparsity Regularization
L1 penalty applied to gate values
Encourages weights to move toward zero
Dynamic λ Scheduling
Gradual increase of sparsity pressure during training
Helps balance learning and pruning
Experiments and Observations
Aspect	Observation
Initial Runs	No pruning observed due to weak sparsity influence
Intermediate Tuning	Over-pruning (collapse to near 100% sparsity) observed
Final Configuration	Achieved controlled sparsity behavior with gradual pruning
Key Insight	Proper scaling of sparsity loss and λ is critical
Results Summary
Metric	Value
Dataset	CIFAR-10
Model Type	Self-Pruning MLP
Layers	4 Prunable Layers
Experiments	Multiple λ configurations
Accuracy Range	~50–56%
Sparsity Behavior	Gradual pruning observed after tuning

Note: Achieving stable sparsity required careful balancing between loss scaling, gate activation, and λ scheduling. This reflects realistic challenges in training sparse neural networks.

Tech Stack

Python 3.10+ · PyTorch · Torchvision · NumPy · Matplotlib
Jupyter Notebook · CIFAR-10 · L1 Regularization · Sigmoid Gates

Key Learnings
Sparsity is highly sensitive to loss scaling and hyperparameters
Removing normalization can destabilize training if not controlled
λ scheduling plays a critical role in avoiding early collapse
Neural networks can learn structured pruning behavior when properly regularized
Debugging model behavior is as important as model design
Conclusion

This project demonstrates a working implementation of a self-pruning neural network capable of learning sparsity during training. Through iterative experimentation and tuning, a balance between model performance and sparsity was achieved.

The results highlight both the potential and challenges of integrating pruning directly into the training process, offering insights into efficient deep learning model design.

Ramanan G
Roll No: 22MIA1150
M.Tech Integrated CSE (Business Analytics)
