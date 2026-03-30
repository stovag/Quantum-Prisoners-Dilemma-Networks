# Quantum Prisoner's Dilemma Simulation

This Jupyter Notebook implements a simulation of the Quantum Prisoner's Dilemma (QPD) game with multiple players, incorporating quantum strategies and knowledge sharing mechanisms. It uses Qiskit for quantum circuit construction and execution, either on a simulator or real quantum hardware.

## Description

The notebook explores a multi-player extension of the Prisoner's Dilemma where one player employs a quantum strategy, while others use classical strategies. Key features include:

- **Strategy Gates**: Quantum gates representing player strategies based on parameters like theta, phi, and lambda.
- **Payoff Calculation**: Custom payoff matrices for cooperation and defection.
- **Knowledge Sharing**: Optional sharing of quantum states between games via entanglement.
- **Experimentation**: Runs simulations for different quantum players in a network defined by an adjacency matrix.
- **Logging**: Outputs game results, payoffs, and statistics to a CSV file.

The simulation supports both simulated (using AerSimulator) and real quantum processing unit (QPU) modes.

## Requirements

- Python 3.8+
- Qiskit
- Qiskit Aer
- Qiskit IBM Runtime (for QPU mode)
- NumPy
- Pandas
- NetworkX
- Plotly
- SciPy

## Installation

1. Install required packages:
   ```
   pip install qiskit qiskit-aer qiskit-ibm-runtime numpy pandas networkx plotly scipy
   ```

2. For QPU access, set up your IBM Quantum account and obtain an API token.

## Usage

1. Open the notebook in Jupyter or VS Code.
2. Configure parameters in the main block:
   - `knowledge_sharing`: Boolean for enabling knowledge sharing.
   - `adj_matrix`: NumPy array defining player connections.
   - `logfile`: Path to the output CSV file.
   - `mode`: "simulated" or "qpu".
3. Run the notebook. It will simulate games for each player as the quantum player and log results.
4. Visualize the quantum circuit using `circ.draw(output="mpl")`.

Example output includes average payoffs per player, computed from the logfile.

## Output

- **Logfile**: CSV file with columns for game results, player payoffs, and metadata.
- **Circuit Visualization**: Matplotlib plot of the quantum circuit.
- **Analysis**: Use `get_results()` to compute mean payoffs from the logfile.

## Notes

- Payoff values are arbitrarily chosen for simplicity.
- Ensure the adjacency matrix is symmetric for undirected graphs.
- For QPU mode, replace the token with your own and select an available backend.

```markdown
```
