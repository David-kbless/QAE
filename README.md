# QAE
Reproduction du pricing d’un call européen par Quantum Amplitude Estimation

The goal of this project is to design a quantum circuit that leverages the Quantum Amplitude Estimation algorithm to approximate the price of a call option. More precisely, given a call option with strike $K$ and maturity $T$ on an underlying $S$ with volatility $\sigma$, the goal of this project is to design a circuit that constructs a state of the form
$$\sqrt{1-a}\left(|\Psi_0\rangle_n \otimes |1\rangle\right) + \sqrt{a}\left(|\Psi_1\rangle_n \otimes |1\rangle\right)$$
such that $a$ is an approximation of $\mathbb{E}\left[(S_T - K)_+\right]$. The Quantum Estimation Algorithm is then used to estimate the value of $a$, which represents the *compounded* price of the call option.
