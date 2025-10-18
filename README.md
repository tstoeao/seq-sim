# SEQ-Sim: TSTOEAO Equilibrium Persistence Simulations

## Overview
This repo implements the core simulations for the Swygert Theory of Everything AO (TSTOEAO), focusing on the Swygert Equilibrium Quotient (SEQ) and Evolutionary Persistence Quotient (EPQ). 

- **Null Model**: Standard stochastic logistic growth (primordial soup baseline) – ~62% persistence rate.
- **Modulated Model**: EPQ-applied damping outside equilibrium bands [0.65, 0.80], boosting stability to ~87% via encoded equilibrium (V = E × Y yield).

Derived from TSTOEAO papers (e.g., Zenodo 17376414). Tests substrate encoding for bio/cosmo persistence: mutations culls non-eq states, favoring resonant modes.

## ## Setup & Run
1. Clone: `git clone https://github.com/tstoeao/seq-sim.git`
2. Install deps: `pip install numpy matplotlib` (Python 3.8+)
3. Run: `python main.py`

Outputs:
- Console: Stability % (seeded for repro).
- `seq_sim_results.png`: Traj samples + final dists (modulated peaks in eq band).

## Theory Tie-In
- EPQ = PQ × (1 – μ ΔDQ): Modulates growth dx/dt = r x (1 - x/K) outside band.
- Falsifiable: Tune noise_std; expect modulated > null by 20-30% (verifies AO causality).
- Extends to LIGO/SEQ: Analog for wave strain equilibria (future: port to gwpy).

## License
MIT – Fork, extend, unify.

Questions? @tstoeao on X. Cite: Swygert (2025), TSTOEAO MDDF.
