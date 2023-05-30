# Elementary Cellular Automata State Transition 

This Python script simulates elementary cellular automata based on a given rule and width. It supports two types of boundary conditions: periodic and null.

## Getting Started

1. Click on the "Open in Colab" button to open the notebook in Google Colab.
2. Follow the instructions in the notebook to enter the rule and width for the cellular automata simulation.
3. Run the notebook cells to execute the code and visualize the simulation results.

## Customization

- Rule: Enter a string of 8 binary digits (e.g., "01011010") to define the rule for the cellular automata.
- Width: Specify the number of cells (width) in the cellular automata.

## Results

The script will generate a table that shows the evolution of the cellular automata for each boundary condition and initial configuration. The table includes the generation number and the state of each cell.

## Additional Notes

In transition diagrams of elementary cellular automata, there are three possible behaviors for generations:

- Loop: The generations can form a repeating pattern where the same configuration is encountered again after a certain number of iterations. This can result in a stable or oscillating behavior where the automaton reaches a steady state or alternates between multiple states.
The script includes a condition to stop generating generations if the current generation matches the initial configuration it started from. This is assumed to indicate looping.

- End at Zero: The generations can eventually reach a state where all cells have a value of zero. This means that the automaton has converged to a homogeneous state where all cells are inactive.
The script includes a condition to stop generating generations if the current generation matches the quiescent state. This is assumed to indicate the end at zero behaviour.

- Chaotic: The generations can exhibit a chaotic behavior where there is no discernible pattern or repetition. In this case, the automaton evolves in a seemingly random manner, and it is difficult to predict or analyze its long-term behavior.
The script includes a condition to stop generating generations if it exceeds a certain number (50) for the boundary conditions. This is assumed to indicate chaotic dynamics.

- The script utilizes the `tabulate` library to display the simulation results in a tabular format.
