# Graph Coloring using Genetic Algorithms

**Author:** Adrian Mateos Garza
**GitHub:** [@AdrianMateosG](https://github.com/AdrianMateosG)

## Overview

This project implements a genetic algorithm to solve the Graph Coloring Problem (GCP), which is a well-known NP-hard problem in computer science and mathematics. The goal is to assign colors to vertices of a graph such that no adjacent vertices share the same color, while using the minimum number of colors possible.

## How it Works

### The Algorithm

The implementation uses a genetic algorithm with the following components:

1. **Population Initialization**: Random valid color assignments for each vertex
2. **Fitness Function**: Evaluates solutions based on the number of correctly colored vertices (no adjacent vertices sharing the same color)
3. **Selection**: Roulette wheel selection method to choose parent chromosomes based on fitness
4. **Crossover**: Single-point crossover with configurable probability
5. **Mutation**: Random color reassignment with low probability to maintain diversity
6. **Stop criterion**: Algorithm stops once it has found a feasible solution given the number of colors

### Input

- Graph structure in a spreadsheet format (adjacency matrix), such as CSV, XLSX, or any format accepted by pandas.
- Configurable parameters:
  - Population size
  - Number of colors
  - Mutation rate
  - Crossover rate
  - Maximum iterations

### Output

- List of feasible solutions found
- Best solution with its fitness value
- Visualization of colored graph
- Computation time

### Solution Representation

Solutions are represented as lists where each index corresponds to a vertex in the graph, and the value at that index represents the color assigned to that vertex. For example, in a solution `[1, 2, 3, 1]`, vertex 0 is colored red, vertex 1 is green, vertex 2 is blue, and vertex 3 is red.

The available colors are (maximum 8):

1. Red
2. Green
3. Blue
4. Purple
5. Cyan
6. Yellow
7. White
8. Gray

A solution is considered valid (feasible) when no adjacent vertices share the same color.

## Requirements

- Python 3.7+
- pandas
- numpy
- networkx
- matplotlib

## Usage

1. Prepare your graph in adjacency matrix format (CSV, XLSX, etc.)
2. Run the notebook
3. The algorithm will find a valid coloring using the specified number of colors
4. Results will show:
   - Statistics about the solutions
   - Best solution found
   - Feasible solutions if any
   - A visualization of the colored graph

## License

This project is licensed under the MIT License.
