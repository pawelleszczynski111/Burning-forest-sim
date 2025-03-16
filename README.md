# Forest Fire Simulation

## Project Overview
This project is a simulation based on an evolving cellular automaton, designed to model the spread of fire in a forest. The simulation incorporates various environmental factors such as wind, water barriers, and regrowth of trees after burning. The model is governed by a set of predefined rules that dictate how fire spreads and how the environment evolves over time.

![ezgif-25cb35041149f0](https://github.com/user-attachments/assets/4e56ef6a-fc80-4c75-b284-daccc320c851)


## Simulation Assumptions

1. **Cell States:** Each cell in the simulation grid can exist in one of four states:
   - **Tree**: A healthy tree.
   - **Burning Tree**: A tree that is currently on fire.
   - **Burned Tree**: A tree that has been burned down.
   - **Water**: A water cell that acts as a fire barrier.

2. **Fire Initiation:** The first burning tree is created through spontaneous combustion of a randomly selected tree on the map.

3. **Spontaneous Ignition Probability:** Trees have a configurable probability of self-ignition, representing external factors such as lightning strikes.

4. **Fire Spread:**
   - A tree can catch fire from a neighboring burning tree with probability `p`.
   - If a tree has multiple burning neighbors, each ignition attempt is checked separately. For example, if a tree has two burning neighbors, it has two chances to ignite.

5. **Burning Process:** A burning tree transitions to a burned tree in the next generation.

6. **Tree Regrowth:** After `k` generations, a burned tree regrows into a new tree.

7. **Fire Barriers:** Water cells act as barriers and prevent fire from spreading.

8. **Wind Effects:**
   - Wind can either be absent or blow in one of four cardinal directions (North, South, East, West).
   - The wind has four different intensity levels.
   - Wind can randomly change its direction and intensity in each generation.
   - Wind increases the probability of ignition in its direction by `s` and decreases the probability of ignition in the opposite direction by `s`.

9. **Simulation Termination:** The simulation ends when no burning trees remain on the map.

## Features
- Configurable parameters:
  - Probability of spontaneous ignition.
  - Probability of fire spreading between trees.
  - Number of generations required for tree regrowth.
  - Wind strength and direction.
- Randomized environmental factors, including wind behavior.
- Visualization of the forest fire spread over time.
- Efficient grid-based implementation using cellular automaton principles.

## Installation & Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/forest-fire-simulation.git
   cd forest-fire-simulation
   ```
2. Run the simulation:
   ```sh
   python main.py
   ```
3. In function ,,contro_functio()" you are able to modify simulation conditions

   ![awdaw](https://github.com/user-attachments/assets/fc3c30ae-6da3-486e-ad9a-ccb0039b3a91)


## License
Feel free to use and modify it for your own research and simulations.


---
Developed by **Paweł Leszczyński**

