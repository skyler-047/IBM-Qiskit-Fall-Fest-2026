# IBM-Qiskit-Fall-Fest-2026

# Project Title

Correlations, Step Size, Error Scaling, Depth Trade-offs, and Second-Order Formula in Transverse-Field Ising Model Trotterization


# Project Summary

This project follows the beginner level of track 3 Quantum Dynamics challenge and studies all four directions provided: correlations, Trotter step size, accuracy vs. depth, and higher-order Trotter.

For the first direction, I computed the two-point correlation function and its connected version for first-order Lie-Trotterization and then plotted them as heatmap animations and distance-averaged heatmaps. From the figures, it can be seen that the connected correlations are strongest between nearby qubits and weaker at larger distances, and that the connected correlation shows a trend to spread to qubits that are farther apart at the beginning of the simulation. This suggests that information first builds up locally and then spreads outwards, while the mutual influence between more distant qubits is smaller.

For the other directions, I first calculated the averaged total magnetization along the z-axis of first-order Lie-Trotterization and then the error scaling, finding that the error scaling is not what we expected. I realized that it's actually because first-order and second-order methods are mathematically the same in this setup, so I then changed the observable to magnetization along the x-axis, and the results then turned out to match the expectation. 

After that, I studied the effect of smaller Trotter sizes on the accuracy of the results, plotted the max error against the total number of two-qubit gates, and then compared the outcomes of first-order Lie-Trotterization and second-order Suzuki-Trotterization. As expected, smaller dt gives lower error, but it also comes with more Trotter steps and deeper circuits, so there is a clear trade-off between accuracy and depth. Comparing the two methods, second-order Suzuki-Trotter reaches the set accuracy threshold with fewer two-qubit gates, so in our setup the higher-order formula is a better method.

# Files Overview

Correlation and Connected Correlation.ipynb investigates the correlation function and its connected version of first-order Lie-Trotterization.
Step Size, Error Scaling, Depth Trade-offs, and Second-Order.ipynb studies how the accuracy of the results change with different trotter sizes, the error scaling, the trade-off between error and the total amount of two-qubit gates, and the comparison between first-order Lie-Trotterizatioin and second-order Suzuki-Trotterization.


# AI Disclosure

Generative AI is used for some debugging tasks, assisting in learning, and some final error checks. AI translation tool (DeepL) is also used to help organize language for some part.
