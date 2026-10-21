# Methodology and interpretation guide

## Study design

The project uses anonymous Yoochoose click and purchase sessions to construct behavioral sequences. It progressively studies descriptive state transitions, latent-state models, sequential decisions, reinforcement learning, and partial observability.

## Behavioral representations

The main DTMC/CTMC representation contains three transient states and two absorbing states:

- `Browsing`
- `Engaged`
- `HighIntent`
- `Buy`
- `Exit`

Additional notebooks use nine activity-speed combinations such as `Low_Fast`, `Medium_Normal`, and `High_Slow`.

These states are analytical representations defined by the project. Their names provide business interpretations, but they are not direct psychological measurements.

## Evidence levels

### Empirical descriptive analysis

The DTMC and CTMC chapters estimate transitions and absorption behavior from selected Yoochoose sessions under the project's state definitions.

### Model-based exploration

The HMM chapter studies hidden-state algorithms and sequence likelihoods using derived observations.

### Scenario simulation

The MDP, Value Iteration, RL, and POMDP chapters introduce specified actions, transition effects, rewards, or simulated trajectories. Policies learned in these environments are conditional on those assumptions.

## Responsible interpretation

Results should be phrased as:

- “estimated under the selected state construction,”
- “observed on the analyzed sample,”
- “obtained in the modeled environment,” or
- “exploratory simulation result.”

They should not be phrased as proven causal improvements, guaranteed conversion uplift, or validated production performance without an intervention dataset or controlled experiment.

## Reproduction boundaries

The public repository excludes the raw dataset and preserves the original notebook implementation. Users must configure dataset paths and execution environments locally. GPU-backed sections may require Google Colab or an equivalent CUDA environment.

