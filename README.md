# Quantum Computing - Assignment 1

**Author:** Sneha Shinde 

**Program:** PGP in AI & Data Science, Jio Institute 

**Quarter:** 5 - Quantum Computing  

---

## 📌 Overview

This repository contains the implementation of two fundamental quantum communication protocols using **Qiskit**:

- Quantum Teleportation (Fully Unitary Implementation)
- Superdense Coding

All circuits are executed and verified using the **Qiskit Aer Simulator**.

---

## 📂 Repository Structure

- `SnehaShinde_Assignment_1_Problem_1_Part_A.ipynb` – Quantum Teleportation code  
- `SnehaShinde_Assignment_1_Problem_2_Part_A.ipynb` – Superdense Coding code  
- `Part_B_Conceptual.pdf` – Conceptual answers and discussion  
- `README.md` – Project documentation  

---

## 🔹 Problem 1: Quantum Teleportation  

## Objective  
Teleport an unknown quantum state |ψ⟩ from Alice to Bob using a shared Bell state, utilizing a fully quantum (unitary) correction method instead of classical feed-forward.

---

## Implementation Summary  

1. **State Preparation:** Prepare an arbitrary state  
   |ψ⟩ = Rz(φ) · Ry(θ) |0⟩  
   with θ = 1.2 and φ = 0.8.

2. **Entanglement:** Create a Bell pair |Φ⁺⟩ between Alice and Bob.

3. **Transformation:** Apply the Bell-basis transformation (CNOT on q0, q1 followed by H on q0).

4. **Quantum Correction:** Perform coherent correction using CX and CZ gates.

5. **Verification:** Apply the inverse unitary  
   U† = Rz(-φ) · Ry(-θ)  
   on Bob's qubit (q2).

6. **Measurement:** Measure Bob’s qubit to verify the state has returned to |0⟩.

---

## Result  

- **Simulation (5000 shots):** Bob measured state `'0'` with 100% probability (`{'0': 5000}`).

- **Conclusion:** Teleportation verified successfully.

---

## 🔹 Problem 2: Superdense Coding  

## Objective  
Demonstrate the ability to transmit two classical bits of information by physically sending only one qubit through a shared Bell pair.

---

## Implementation Summary  

1. **Entanglement:** Create a Bell pair |Φ⁺⟩ using H and CNOT gates.

2. **Encoding:** Alice encodes the message `'11'` using an X gate followed by a Z gate on her qubit.

3. **Decoding:** Bob receives the qubit and decodes it using a CNOT and a Hadamard gate.

4. **Measurement:** Measure both qubits to retrieve the 2-bit message.

---

## Result  

- **Simulation (1000 shots):** The circuit accurately returned the message `'11'` for all shots (`{'11': 1000}`).

- **Conclusion:** Superdense coding verified successfully.

---

## 🛠 Tools & Requirements  

- **Language:** Python  
- **Libraries:** qiskit, qiskit-aer, matplotlib, numpy  

### Installation  

```bash
pip install qiskit qiskit-aer matplotlib numpy
```

---

## 📖 Key Concepts  

- **Bell States:** Maximally entangled two-qubit states.  
- **Unitary Correction:** Replacing classical communication with quantum controlled gates.  
- **Entanglement-Assisted Communication:** Using quantum resources to enhance classical data transfer.  

---

## 📝 License

*Submitted as part of academic coursework at Jio Institute.*
