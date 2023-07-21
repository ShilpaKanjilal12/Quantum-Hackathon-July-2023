# Quantum-Hackathon-July-2023

## Quantum Key Distribution

### Introduction

Quantum Key Distribution (QKD) is a secure method of establishing cryptographic keys between two parties, such as Alice and Bob, who want to communicate securely. Unlike classical cryptographic methods, QKD uses the principles of quantum mechanics to generate and distribute encryption keys. The most widely used QKD protocol is the BB84, which was proposed by Charles Bennett and Gilles Brassard in 1984.


### About this project:

My primary objective was to implement a secure quantum key distribution (QKD) method using Qiskit dm_simulator. A BB84 QKD protocol is  utilize for generating and distributing keys securely, with a focus on maximum randomness and secrecy to resist potential eavesdropping attacks.

#### High-level outline:

1. Quantum State Preparation by Alice and Transmission from Alice to Bob:
- Generate a sequence of random bits to represent the secret key.
- Prepare quantum qubits corresponding to the random bit values in random bases (X or Z).
- Send the prepared qubits to Bob over a communication channel.

2. Bob's measurement 
- Bob randomly chooses to measure each qubit in either the X-basis or the Z-basis.

3. Basis Announcement and Key Sifting:
- Alice and Bob publicly reveal the bases they used for each qubit over a classical channel.
- They keep the bits for which their bases match, forming a sifted key.
- The sifted key contains bits that they measured in the same basis.

4. Privacy Amplification (Classical Post-processing):
- Alice and Bob perform Privacy Amplification on the sifted key to obtain a secured secret key. Here I have used the SHA-256 (Secure Hash Algorithm 256-bit) which is a widely used cryptographic hash function.

5. Secure Communication (For Demonstrating the use of the final key):
- The final secret key can be used for encryption to enable secure communication between Alice and Bob.

