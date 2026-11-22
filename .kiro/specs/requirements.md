# Q-Macro Chimera — Requirements Specification

## Overview
A Frankenstein financial risk workbench that fuses classical Monte Carlo Value-at-Risk (VaR) simulation with quantum-inspired / quantum amplitude estimation circuits, verified by property-based tests.

## Functional Requirements
1. **Portfolio Input:** Accept portfolio asset weights, expected returns, volatilities, and confidence level (e.g., 95%, 99%).
2. **Classical Engine:** Run classical Monte Carlo simulation to compute VaR and Expected Shortfall (CVaR).
3. **Quantum Chimera Engine:** Run a simulated quantum circuit / amplitude-estimation risk estimator on the same distribution and compare convergence vs. classical paths.
4. **Property-Based Invariants:**
   - All probability distributions sum to `1.0` within floating-point tolerance.
   - VaR is monotonically non-decreasing with confidence level (`VaR_99 >= VaR_95`).
   - Portfolio volatility and VaR remain invariant under asset ordering permutations.
