# Safe RL for MiniGrid: PPO with Hamilton-Jacobi Safety Critic

Implemented safety-constrained reinforcement learning by integrating PPO with a safety Q-network using a modified Bellman operator based on Hamilton-Jacobi reachability analysis.

## Key Results
- 40% reduction in constraint violations through safety shielding
- Demonstrates safety-performance tradeoff in constrained RL

## Technical Details
- **Environment**: MiniGrid LavaCrossingS9N1-v0
- **Task Policy**: PPO (Stable-Baselines3)
- **Safety Critic**: Custom Q-network (PyTorch)
- **Innovation**: Modified Bellman operator `Q(s,a) = min(cost, γ·max_a' Q(s',a'))`

## Based On
Fisac et al., "Bridging Hamilton-Jacobi Safety Analysis and Reinforcement Learning"  
[IEEE Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8794107)
