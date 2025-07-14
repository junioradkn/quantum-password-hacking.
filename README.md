# quantum-password-hacking.
QUANTUM PASSWORD HACKING: USING GROVER'S ALGORITHM TO SOLVE PASSWORDS


By Eli Kim, Junior Adoukonou, Miyu Umemoto, Keith Wallington

This project demonstrates the use of Grover's quantum search algorithm to locate a hidden password out of a finite number of possible candidates and achieve a quadratic speedup over classically brute-forced search. We implement the algorithm in Google Cirq, simulate the impact of altering the number of iterations on success probability, test scalability to larger password spaces such as 4-bit passwords, and test robustness by adding noise.

python grover_basic.py
to see Grover’s algorithm search for a known password (like '11').

To run the generalized version that searches for a hidden random password:
python grover_generalized.py

For testing with a larger 4-bit password space, run:
python grover_4bit.py

And to simulate noise, run:
python simulate_noise.py



LITERATURE REVIEW

How can Grover's quantum search algorithm efficiently find a password within a limited search space? 

How does its performance compare to classical brute-force search, especially when dealing with larger search spaces and noise?

This project examines how Grover's algorithm can search for hidden passwords more effectively than traditional brute-force methods by providing a quadratic speedup. We will implement and test Grover's algorithm in Google Cirq for 3-bit and 4-bit password search spaces. We will check its success rate with different numbers of iterations and simulate noise to explore its practical limits. Our goal is to look at both the possibilities and current challenges of quantum search for real-world tasks like password cracking. 

As digital systems increasingly rely on passwords and cryptographic keys for security, the ability of quantum computers to break these protections has gained significant attention. Traditional brute-force methods check each password one after another, leading to exponential growth in time as passwords get longer. Grover's quantum search algorithm reduces the search complexity from O(N) to O(sqrtN). This poses a serious threat to traditional password security. 

This project explains how Grover's algorithm is used for password cracking, why it matters for cybersecurity, and the practical challenges in applying it to larger and noisier systems. Discovered by Lov Grover in 1996, Grover's algorithm is one of the most important quantum algorithms due to its potential to speed up unstructured search tasks. Unlike Shor's algorithm, which threatens cryptographic systems based on the factoring of large numbers, Grover's algorithm endangers symmetric-key systems and password security by providing a quadratic speedup over traditional brute-force searches. 

Grover's algorithm uses quantum parallelism and amplitude amplification to improve the chances of finding the correct answer after about sqrtN iterations, where N is the number of possible passwords. Previous research and simulations have shown Grover's theoretical effectiveness, but practical limitations for real-world applications still exist. Implementing Grover's algorithm requires an oracle to mark the correct password with a phase flip and a diffusion operator to redistribute amplitude. Although these components can be developed and tested in quantum simulators like Google Cirq or IBM Qiskit, running them on actual quantum hardware introduces noise and errors that significantly lower the chances of success. Recent studies have explored error reduction techniques and noise-resistant circuit designs, but scaling beyond small search spaces remains computationally challenging due to current quantum technology.

Additionally, the literature shows that while Grover's algorithm reduces search complexity, it also requires a large number of quantum gates and precise coherence times, which strains today's quantum processors. Researchers have looked into variations of Grover's algorithm, like multi-solution oracles and adaptive iteration methods, to address these issues. By simulating and adjusting Grover's search for password cracking, this project aims to connect theoretical quantum speedup with real-world implications, shedding light on where quantum computing can impact cybersecurity and where further development is necessary.



PRELIMINARY DATA

We worked on Grover’s algorithm on a quantum computer to search for obscured passwords. We started with a basic version using 2-qubits to search for a previously-specified password (“11”) and then progressed to a version able to search for any 3-bit password such as “101,” “000,” or “111.” Our circuit layout contained an oracle that indicated the proper password by phasing, and a diffuser that increased the odds in getting the right answer. We varied the number of iterations (repeats) in testing the algorithm in order to observe the effect on the success rate, and we repeated the circuit in order to provide data for various passwords. 

The early findings are that Grover's algorithm is best for running the optimal number of times—the 3-bit password algorithm for running 2 iterations. The algorithm for running for far too long, however, makes the success rate fall because of the variation in the odds naturally. We learned from all the above that iterations do count for Grover's performance, and when well done, the algorithm always reveals unique passwords but at the same speed. Future directions include scaling our method for 4-bit passwords, predicting the effect of noise and errors in the circuit, and pitting our quantum findings against a classical brute-force search for an estimate on the number of practical advantages in running the quantum technique.

