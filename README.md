# quantum-password-hacking.
Research Question
Can Grover’s algorithm find a hidden password faster than a regular computer trying every possible guess, and how does noise in a quantum computer affect its success?

Overview
This project shows how Grover’s algorithm, a special quantum method, can guess a password faster than classical methods. Instead of testing each password one by one like a normal computer, Grover’s algorithm uses quantum effects to check many possibilities at once and needs only about the square root of the total guesses.

We will use Google Cirq, a tool that simulates quantum computers on a regular computer, to build and run this quantum password search.


Abstract (2–3 sentences)
This project investigates whether Grover’s algorithm can guess a password faster than classical methods. Using Google Cirq, we test its performance in ideal and noisy conditions to see how quantum noise affects its success.

Draft Introduction Paragraph
Grover’s algorithm promises a faster way to search through data by using quantum mechanics. In password guessing, it can reduce the number of tries needed from N to about √N. But real quantum computers have noise, which may reduce this advantage. This paper explores whether Grover’s algorithm still outperforms classical search when noise is present.

Literature Review (3 Short Paragraphs)
1. Grover’s Algorithm Basics
Grover’s algorithm uses quantum parallelism to find a marked item in O(√N) steps, offering a clear speed-up over classical brute-force search.

2. The Challenge of Quantum Noise
Noise in quantum systems—like decoherence and gate errors—can reduce the accuracy of quantum algorithms, including Grover’s. Too much noise can cause the algorithm to fail.

3. Using Google Cirq
Cirq lets us build and test quantum circuits in simulation. It includes tools to add noise, helping us study how Grover’s algorithm performs under realistic conditions.

Relevant research papers:
1. Noise in Grover’s Quantum Search Algorithm
Authors: B. Pablo‑Norman & M. Ruiz‑Altaba (1999)

This paper studies how Grover’s algorithm behaves when random Gaussian noise is applied at each step. It derives analytical bounds showing that noise tolerance scales with the database size as N^(–2/3). The authors identify a critical noise level where Grover’s quantum advantage disappears, making it no faster than classical brute-force search.

 2. Noise‑Tolerant Grover’s Algorithm via Success‑Probability Prediction
Authors: Jian Leng, Fan Yang & Xiang‑Bin Wang (2025)

This recent paper proposes a modified version of Grover’s algorithm that predicts optimal stopping points based on success probability, improving resilience to noise. The method shows significantly higher noise tolerance and fewer iterations needed, preserving quantum speed-up on noisy intermediate-scale quantum (NISQ) hardware. The results are validated both theoretically and through simulations.
