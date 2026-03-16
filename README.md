# QKD-Simulation-Basic

# Quantum Key Distribution (QKD) Simulation using BB84 Protocol

## Overview

This project simulates **Quantum Key Distribution (QKD)** using the **BB84 Protocol**, one of the most widely studied quantum cryptography protocols. The simulation demonstrates how two parties (Alice and Bob) can securely generate a shared secret key using principles of quantum mechanics, while detecting the presence of an eavesdropper (Eve).

The implementation models the complete QKD workflow including:

- Random bit generation
- Random basis selection
- Quantum transmission simulation
- Eavesdropping attack simulation
- Key sifting
- Quantum Bit Error Rate (QBER) calculation
- Error correction
- Privacy amplification
- Experimental statistical analysis
- Data visualization

The project is implemented entirely in **Python** and runs on **CPU only**, making it suitable for execution in **Google Colab**, **Jupyter Notebook**, or a local Python environment.

---

## Key Concepts

### Quantum Key Distribution (QKD)

Quantum Key Distribution is a secure communication method that uses **quantum mechanics** to generate and distribute cryptographic keys. Unlike classical encryption methods, QKD can detect eavesdropping because measuring quantum states disturbs them.

### BB84 Protocol

The **BB84 protocol**, proposed by Charles Bennett and Gilles Brassard in 1984, uses two sets of quantum bases:

- **Rectilinear Basis (+)**  
- **Diagonal Basis (×)**  

If the receiver measures a photon using the wrong basis, the result becomes random. This property helps detect interception attempts.

### Quantum Bit Error Rate (QBER)

QBER measures the percentage of mismatched bits between Alice and Bob after transmission. A high QBER indicates potential interference or eavesdropping.

---

## Project Features

- Full simulation of the **BB84 QKD protocol**
- **Intercept-Resend attack simulation** by Eve
- **QBER computation**
- **Key sifting mechanism**
- **Simplified error correction**
- **Privacy amplification using SHA-256 hashing**
- **Multiple experiment runs for statistical analysis**
- **Graph visualization of experiment results**

---

## Technologies Used

| Technology | Purpose |
|------------|--------|
| Python | Core programming language |
| NumPy | Random bit generation and numerical operations |
| Pandas | Data analysis and experiment logging |
| Matplotlib | Visualization of results |
| Hashlib | Privacy amplification using cryptographic hashing |

---

## Project Structure

```

QKD-Simulation/
│
├── qkd_simulation.ipynb      # Jupyter notebook implementation
├── README.md                 # Project documentation

````

---

## Installation

Install the required Python libraries:

```bash
pip install numpy pandas matplotlib
````

---

## Running the Project

### Option 1: Google Colab

1. Open Google Colab
2. Create a new notebook
3. Paste the project code into a cell
4. Run all cells

### Option 2: Jupyter Notebook

Start the notebook server:

```bash
jupyter notebook
```

Open the project notebook and execute all cells.




## Simulation Workflow

The simulation follows these steps:

1. **Alice generates random bits and bases**
2. **Photons are transmitted through a simulated quantum channel**
3. **Eve optionally performs an intercept-resend attack**
4. **Bob randomly chooses measurement bases**
5. **Alice and Bob perform key sifting**
6. **QBER is calculated**
7. **Error correction is applied**
8. **Privacy amplification compresses the key**
9. **Multiple experiments are executed for statistical analysis**
10. **Results are visualized**

---

## Example Output

Console output example:

```
Run 1
QBER: 0.24
Key Length: 5012
Sample Secret Key: a82b34bfae...

Run 2
QBER: 0.25
Key Length: 4987
```

---

## Visualization Results

The simulation generates three plots:

### 1. QBER vs Experiment Run

Shows how the Quantum Bit Error Rate varies across multiple runs.

### 2. Key Length vs Experiment Run

Displays the size of the final sifted key in each experiment.

### 3. QBER Distribution

Histogram showing how QBER values are distributed across experiments.

---

## Security Analysis

The simulation demonstrates how QKD detects eavesdropping:

* If Eve intercepts photons, measurement errors increase.
* This causes the **QBER to rise above normal thresholds**.
* Alice and Bob can then discard the compromised key.

Typical secure QKD systems maintain QBER below approximately **11%**.

---

## Possible Extensions

This project can be extended to simulate more realistic quantum communication scenarios:

* Photon loss and attenuation in optical fiber
* Quantum channel noise models
* Distance vs QBER analysis
* Multi-node quantum networks
* Entanglement-based QKD protocols (E91)
* Quantum network simulation
* Integration with quantum computing frameworks

---

## Applications

Quantum Key Distribution has potential applications in:

* Government secure communication
* Financial transaction security
* Satellite quantum communication
* Military-grade encryption
* Quantum internet infrastructure

---

## Author

Arka Singha

---

## License

This project is intended for educational and research purposes.

```
```
