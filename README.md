# HousePricePrediction
A house price prediction system according to the size of the house is made using Linear Regression, for the completion of my second assignment under the academic  ml course.

Project Overview:

This project demonstrates how Linear Regression works:

Implemented from scratch using Gradient Descent.

Compared with Scikit-learn’s LinearRegression for validation.

The goal is to understand what happens behind the scenes in Linear Regression and verify correctness by comparing with the scikit-learn implementation.

⚙️ How Things Work
1. Dataset

We generate synthetic data using make_regression from scikit-learn.

The dataset has input features X and a target variable y.

👉 Think of it as predicting output y given some input X.

2. Linear Regression from Scratch

We build a custom Linear Regression model using Gradient Descent.

Steps:

Initialize Parameters: Start with random weights and bias.

Prediction: Compute

𝑦
^
=
𝑋
𝑊
+
𝑏
y
^
	​

=XW+b

where 
𝑊
W = weights, 
𝑏
b = bias.

Loss Function: Use Mean Squared Error (MSE) to measure error between predicted and actual values.

𝑀
𝑆
𝐸
=
1
𝑛
∑
(
𝑦
−
𝑦
^
)
2
MSE=
n
1
	​

∑(y−
y
^
	​

)
2

Gradient Descent Update: Adjust weights & bias to minimize error.

𝑊
:
=
𝑊
−
𝛼
⋅
∂
𝑀
𝑆
𝐸
∂
𝑊
,
𝑏
:
=
𝑏
−
𝛼
⋅
∂
𝑀
𝑆
𝐸
∂
𝑏
W:=W−α⋅
∂W
∂MSE
	​

,b:=b−α⋅
∂b
∂MSE
	​


where 
𝛼
α = learning rate.

Repeat for many epochs until the loss reduces.

3. Training Visualization

We plot Epoch vs Loss to see how the model improves over time.

Loss decreases gradually → shows Gradient Descent is working.

4. Scikit-learn Linear Regression

We fit LinearRegression() on the same dataset.

This uses the Normal Equation (analytical solution) instead of Gradient Descent.

Formula used:

𝑊
=
(
𝑋
𝑇
𝑋
)
−
1
𝑋
𝑇
𝑦
W=(X
T
X)
−1
X
T
y
5. Comparison of Results

Print learned weights and bias from both models.

If the scratch model works correctly, its parameters should be very close to scikit-learn’s.

📊 Output Example

Loss Curve: Shows convergence of Gradient Descent.

Weights & Bias: Nearly same values from both scratch & scikit-learn models.

🚀 Key Learning Outcomes

Understand how Linear Regression actually works (not just using libraries).

Learn how Gradient Descent optimizes parameters.

Verify correctness by comparing with scikit-learn’s solution.

🛠️ Requirements

Python 3.x

NumPy

Matplotlib

scikit-learn

Install via:

pip install numpy matplotlib scikit-learn

▶️ How to Run
python linear_regression_scratch.py
