# quantum-password-hacking.
QUANTUM PASSWORD HACKING: USING GROVER'S ALGORITHM TO SOLVE PASSWORDS


By Eli Kim, Junior Adoukonou, Miyu Umemoto

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



