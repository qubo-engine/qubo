QUBO Engine & Beno-Engine: High-Performance Optimization & Neuro-Symbolic AI
🚀 High-Performance Optimization, QUBO Solvers & Neuro-Symbolic AI Systems
Welcome to QUBO Engine / Beno-Engine! A cutting-edge industrial-grade decision-making and optimization suite built from scratch in Rust and Python.
📊 Core Performance Benchmarks
1. Aviation Disruption Management (Air France ROADEF Challenge)
Stress test parameters: 50 scheduled flights, 10 aircraft (Narrow & Wide-body fleet mixture), dual-airport severe weather blockades (CDG departure ban & LHR morning fog), and strict European Union Aviation Safety Agency (EASA) crew duty limits (840-minute maximum shifts).
Optimization Level
Completed Flights
Cancelled Flights
Fleet Adjustments
Financial Outcome
Pure MCTS (Greedy Approach)
27 / 50
23
0 Ferry / Deadhead
📉 -1,240,013.50 € (Severe Loss)
Beno-Engine (Move Ordering + Ferry Flights)
36 / 50
14
10 Prázdne Prelety
📈 -596,579.50 € (52% Cost Reduction)
•
Key Breakthrough: Beno-Engine autonomously discovered the economic viability of executing Ferry/Deadhead flights (positioning empty aircraft) to break geographic lock-in traps, saving the airline over 640,000.00 € in a single operational window.
2. Autonomous Last-Mile Drone Delivery (Dynamic Urban Space)
Stress test parameters: Multiple dynamic orders with variable payloads, strict customer delivery SLA time windows, rapid battery charging delays (hardware bottleneck), and stochastic wind gusts changing flight dynamics every 10 minutes.
•
SLA Delivery Success Rate: 100% (All packages delivered within time windows)
•
Safety Margin Integration: Safely managed drone state-of-charge (SoC), forcing proactive charging maneuvers to counter adverse headwind vectors.
•
Net Fleet Profit: +150.00 € in a dense 40-minute simulation window.
📐 Mathematical Formulation & Theoretical Foundations
1. Quadratic Unconstrained Binary Optimization (QUBO)
The core engine optimizes combinatorial problems mapped to the quadratic energy function: $$E(x) = x^T Q x = \sum_{i} Q_{ii} x_i + \sum_{i < j} Q_{ij} x_i x_j$$ where $x_i \in {0, 1}$ and $Q$ is an upper-triangular or symmetric coefficient matrix representing problem costs and constraints.
2. Ternary Qutrit Restricted Boltzmann Machines (RBMs)
Extending standard binary spin glasses to 3-state qutrits: $${-1, 0, +1}$$ This allows the engine to capture neutral / null decision states, frustration minimization, and multi-state Ising rings with high efficiency: $$E(s) = \sum_{i,j} W_{ij} s_i s_j \quad \text{kde } s_i \in {-1, 0, +1}$$
🛠️ Core Technologies & Tech Stack
•
Systems Programming: Rust (qubo_engine.rs, Tokio, Rayon, Ndarray, Bitboards)
•
Mathematical Optimization: QUBO, Ternary Qutrit RBMs (${-1, 0, +1}$), Simulated Annealing, SAT Solvers
•
Artificial Intelligence & Search: Monte Carlo Tree Search (MCTS), Neuro-Symbolic Interpreters, Reinforcement Learning
•
Real-World Applications: Flight Scheduling, Autonomous Drone Delivery Routing, Strategic Game Engines (Chess, Tic-Tac-Toe, ARC AGI)
🧠 Architecture & Engineering Principles
•
qubo-engine (Rust Core): Lightning-fast matrix evaluation and parallel simulated annealing solvers capable of tackling complex combinatorial frustration problems and Ising rings.
•
Neuro-Symbolic Hub: Bridging symbolic logic with neural networks, enabling autonomous multi-agent reasoning, teleology, and decision-making.
•
Constraint Enforcement (get_legal_moves): Ensures 100% validity of physical and regulatory laws before calculating branches.
📂 Project Structure & Key Modules
Module / Script
Description
src/qubo_engine.rs
High-performance Rust QUBO & Qutrit matrix solvers with parallel Simulated Annealing.
src/mcts_engine.rs
Monte Carlo Tree Search engine with move ordering and heuristic pruning.
src/ternary_rbm.rs
Parallel Ternary Qutrit Restricted Boltzmann Machines (${-1, 0, +1}$).
air_france_ai.py
Aviation disruption management & ROADEF challenge simulation dispatcher.
drone_delivery_ai.py
Last-mile drone delivery optimization with battery and weather constraints.
arena_gui.py
Graphical Arena interface for games and agent battles.
🚀 Quick Start & Installation
# Clone and build the Rust QUBO engine
cargo build --release

# Run the advanced Air France business dispatcher
python3 air_france_ai.py

# Run the drone delivery optimization simulation
python3 drone_delivery_ai.py
