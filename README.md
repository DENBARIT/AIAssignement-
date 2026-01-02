### Extended LSTM Cell Implementation (From Scratch)

This project demonstrates a manual implementation of an Extended Long Short-Term Memory (LSTM) cell using NumPy, without relying on deep learning frameworks such as TensorFlow or PyTorch.

The purpose of this implementation is educational — to clearly show how LSTM gates and internal states work step-by-step.

###Project Objectives

Implement an LSTM cell from scratch

Understand the internal components of LSTM:

Forget gate

Input gate

Candidate cell state

Cell state

Output gate

Hidden state

Track and visualize how hidden and cell states evolve over time

Provide transparent numerical outputs for learning and analysis

###Key Features

Manual implementation of LSTM equations

Reproducible results using a fixed random seed

Step-by-step gate value inspection

Visualization of:

Hidden state (h)

Cell state (c)

Lightweight and easy to understand

### Technologies Used

Python 3

NumPy

Matplotlib
 ###Project Structure
.
├── Lstm.py        # Main Python script
├── README.md      # Project documentation
 How to Run the Code

1.Clone the repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
2.Install dependencies
pip install numpy matplotlib
3.Run the script
python Lstm.py
 Example Input Sequence
inputs = [5,1.9,2]
The model processes each value sequentially and prints:

Hidden state

Cell state

Forget gate value

Input gate value

Output gate value

Candidate cell value

 Output Visualization

The script generates a plot showing:

Hidden State (h) over time

Cell State (c) over time

This helps visualize how memory is preserved and updated across time steps.

 Mathematical Overview

At each time step, the LSTM computes:

Forget gate

𝑓
𝑡
=
𝜎
(
𝑊
𝑓
[
ℎ
𝑡
−
1
,
𝑥
𝑡
]
+
𝑏
𝑓
)
f
t
	​

=σ(W
f
	​

[h
t−1
	​

,x
t
	​

]+b
f
	​

)

Input gate

𝑖
𝑡
=
𝜎
(
𝑊
𝑖
[
ℎ
𝑡
−
1
,
𝑥
𝑡
]
+
𝑏
𝑖
)
i
t
	​

=σ(W
i
	​

[h
t−1
	​

,x
t
	​

]+b
i
	​

)

Candidate cell

𝑐
~
𝑡
=
tanh
⁡
(
𝑊
𝑐
[
ℎ
𝑡
−
1
,
𝑥
𝑡
]
+
𝑏
𝑐
)
c
~
t
	​

=tanh(W
c
	​

[h
t−1
	​

,x
t
	​

]+b
c
	​

)

Cell state

𝑐
𝑡
=
𝑓
𝑡
⋅
𝑐
𝑡
−
1
+
𝑖
𝑡
⋅
𝑐
~
𝑡
c
t
	​

=f
t
	​

⋅c
t−1
	​

+i
t
	​

⋅
c
~
t
	​


Output gate

𝑜
𝑡
=
𝜎
(
𝑊
𝑜
[
ℎ
𝑡
−
1
,
𝑥
𝑡
]
+
𝑏
𝑜
)
o
t
	​

=σ(W
o
	​

[h
t−1
	​

,x
t
	​

]+b
o
	​

)

Hidden state

ℎ
𝑡
=
𝑜
𝑡
⋅
tanh
⁡
(
𝑐
𝑡
)
h
t
	​

=o
t
	​

⋅tanh(c
t
	​

)

 ###Authors

Samuel Dessalegn — UGR/2304/14

Leul Gebremariam — UGR/3478/15

Yohannes Wale — UGR/1232/14

Yohannes Alemu — UGR/8644/15

###Academic Use

This project is suitable for:

Artificial Intelligence courses

Machine Learning fundamentals

Neural Networks assignments

Understanding LSTM internals conceptually

### License

This project is provided for educational purposes.
You may reuse or modify it with proper attribution.
