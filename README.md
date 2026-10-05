# Pacman AI Search Project

Artificial Intelligence project based on the UC Berkeley Pacman AI framework, developed as part of the Artificial Intelligence course at Harokopio University.

The project focuses on classical search algorithms, heuristic search and multi-agent decision making in the Pacman environment.

## Project Overview

The project explores how intelligent agents can make decisions in maze-based and adversarial environments.

The implemented work included:

- Depth-First Search (DFS)
- Breadth-First Search (BFS)
- Uniform Cost Search (UCS)
- A* Search
- Heuristic search
- Food-search heuristics
- Minimax
- Alpha-Beta Pruning
- Expectimax
- Custom evaluation functions

## Search Algorithms

### Depth-First Search

DFS explores one branch of the search tree as deeply as possible before backtracking.

A stack-based frontier was used to manage unexplored states.

### Breadth-First Search

BFS explores the search space level by level using a queue.

For problems with uniform step costs, BFS finds a path with the minimum number of actions.

### Uniform Cost Search

UCS expands the state with the lowest accumulated path cost.

A priority queue is used to determine which state should be expanded next.

### A* Search

A* combines the accumulated path cost with a heuristic estimate of the remaining cost:

`f(n) = g(n) + h(n)`

The project used heuristic information such as Manhattan distance to guide the search toward promising states.

## Search Performance

A comparison between UCS and A* showed that heuristic search reduced the number of expanded nodes.

| Maze | UCS Nodes Expanded | A* Nodes Expanded |
|---|---:|---:|
| bigMaze | 620 | 549 |
| openMaze | 682 | 535 |

The results demonstrate how heuristic information can improve search efficiency while still finding high-quality solutions.

## Food Search Heuristic

A heuristic was also implemented for the Pacman food-search problem.

The heuristic estimates the remaining cost using the distance between Pacman's current position and the remaining food locations.

For the tested `trickySearch` layout:

| Algorithm | Nodes Expanded |
|---|---:|
| UCS | 16,688 |
| A* with heuristic | 9,551 |

This significantly reduced the explored search space compared with uninformed Uniform Cost Search.

## Multi-Agent Search

The second part of the project focused on decision making in environments with multiple agents.

### Minimax

Pacman is modeled as the maximizing agent while the ghosts are modeled as minimizing agents.

The algorithm searches possible future game states and selects the action that maximizes Pacman's outcome under the assumption that the ghosts act optimally.

### Alpha-Beta Pruning

Alpha-Beta pruning improves Minimax by eliminating branches of the game tree that cannot influence the final decision.

This allows the agent to evaluate the same decision problem more efficiently.

### Expectimax

Expectimax models ghost actions as probabilistic rather than perfectly adversarial.

Instead of always assuming that ghosts select the worst possible move for Pacman, the algorithm evaluates the expected value of their possible actions.

## Evaluation Function

A custom evaluation function was developed to improve Pacman's behavior.

The evaluation considers several characteristics of the game state, including:

- Distance to the nearest food
- Remaining food
- Remaining power capsules
- Distance to ghosts
- Whether ghosts are scared
- Current game score

This allows the agent to make more informed decisions than when using the basic game score alone.

## Technologies and Concepts

- Python
- Artificial Intelligence
- Graph Search
- Heuristic Search
- Priority Queues
- A* Search
- Adversarial Search
- Minimax
- Alpha-Beta Pruning
- Expectimax
- Multi-Agent Systems
- Evaluation Functions

## Academic Context

This project was completed for the Artificial Intelligence course at the Department of Informatics and Telematics, Harokopio University.

The project is based on the UC Berkeley Pacman AI Projects.

The original Pacman framework was developed at UC Berkeley by John DeNero, Dan Klein and contributors.

## Source Code

The implementation source code is intentionally not included in this public repository.

The UC Berkeley Pacman project licensing notice permits educational use and modification but specifically requests that solution code is not publicly distributed.

This repository therefore serves as a portfolio overview of the implemented algorithms, methodology and results without publishing the assignment solutions.

## Attribution

Based on the UC Berkeley Pacman AI Projects:

http://ai.berkeley.edu/
