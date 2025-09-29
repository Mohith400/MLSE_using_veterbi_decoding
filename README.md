# MLSE using Viterbi Algorithm

This project demonstrates the **Maximum Likelihood Sequence Estimation (MLSE)** using the **Viterbi Algorithm** for a communication system operating over an **Inter-Symbol Interference (ISI) channel**.
It includes state diagram visualization, trellis construction, and symbol error rate (SER) performance evaluation for different traceback lengths.

---

## 📌 Project Details

* **Course:** Digital Communication Systems
* **Author:** K. Mohith Prakash
* **Roll No:** 22EC01002

---

## 🔧 System Setup

* **Modulation:** 4-PAM (symbols = {-3, -1, 1, 3})
* **Channel Impulse Response (ISI):**
  [
  F(z) = 0.6 - z^{-1} + 0.8z^{-2}
  ]
* **Channel Memory (μ):** 2
* **Input Length:** 10,000 symbols
* **Noise:** Additive White Gaussian Noise (AWGN)

---

## 📊 Features

1. **State Diagram Generation**

   * Each state represented by two consecutive PAM symbols (μ = 2).
   * Arrows show valid transitions with input/output labels.

2. **Trellis Diagram Construction**

   * Time-expanded representation of states.
   * Allowed states restricted at start and end to enforce zero-tail termination.

3. **Viterbi Algorithm Implementation**

   * Survivor path tracking.
   * Path metric updates with Euclidean distance.
   * Segment-based traceback with different traceback lengths (N).

4. **Performance Evaluation**

   * Symbol Error Rate (SER) vs SNR (0 to 16 dB).
   * Different traceback depths: (N = μ, 2μ, 4μ, 5μ, 10μ).

---

## 📈 Results

* As traceback depth **N ≥ 4μ**, further increase in (N) provides diminishing returns.
* Simulation confirms that **N = 4μ or 5μ** achieves the best trade-off between **latency** and **error minimization**.

The following plot shows SER performance across different traceback lengths:
<img width="647" height="524" alt="image" src="https://github.com/user-attachments/assets/2b50abea-635b-4529-991a-aa3cbd0abb11" />


## 📚 References

* J. G. Proakis, *Digital Communications*, 5th Edition.
* Simon Haykin, *Communication Systems*.
