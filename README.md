# Quantum Random Number Generator

A true random number generator built using quantum superposition via Qiskit, compared against classical pseudorandomness across 1000 samples.

## How it works

A qubit placed in superposition has an equal probability of collapsing to 0 or 1 when measured. Chaining 8 qubits generates numbers from 0–255 that are physically random — not algorithmic.

Classical computers cannot generate true randomness. Python's `random` module uses a deterministic algorithm (Mersenne Twister) — predictable if you know the seed. Quantum randomness has no such weakness.

## Results

Both distributions are uniform across 1000 samples, but the source of randomness is fundamentally different:

- **Classical:** Deterministic algorithm, pseudorandom, range 0–256
- **Quantum:** Physical superposition collapse, truly random, range 0–255 (8 qubits)

## Tech stack

- Python
- Qiskit
- Qiskit Aer (simulator)
- Matplotlib

## Setup

```bash
pip install qiskit qiskit-aer matplotlib
```

## Notebook structure

| Cell | Description |
|---|---|
| Cell 1 | Quantum RNG function — generates a random number using qubit superposition |
| Cell 2 | Generates 1000 quantum random numbers and plots distribution |
| Cell 3 | Generates 1000 classical random numbers and plots distribution |

## Key learnings

- How quantum superposition generates true randomness
- Why classical random numbers are pseudorandom
- How to build and simulate quantum circuits using Qiskit
- Visualising and comparing probability distributions

## Author

Built as a first Quantum Computing project exploring quantum randomness vs classical pseudorandomness.