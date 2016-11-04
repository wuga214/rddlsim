### Progress
1. Data Extraction from RDDL is functional(Done)
2. Domain Reservoir description(Done)
3. Policy for Reservoir(Done)
4. Domain Determinization(Done)
5. store PVAR+TERM to output file(Done)
6. Bug free testing(Done)

### TODO
1. Domain Description for Inventory control and power gen

### New folder to accept data and label output for Neural Network training.

### RUN
Modified run to accept more than 13 parameters

RDDL Interface Improvement
===============================================

# Updated parameter handling

```
*********************************************************
>>> Parameter Description
*********************************************************
[1]: -R: RDDL file or directory that contains RDDL file
[2]: -P: Policy name e.g. rddl.policy.RandomBoolPolicy
[3]: -I: Instance name e.g. elevators_inst_mdp__9
[4]: -V: Visualization Method e.g. rddl.viz.GenericScreenDisplay
[5]: -S: Random seed for simulator to sample output.
[6]: -X: Random seed for policy to take random actions.
[7]: -K: Number of rounds. Default:1
[8]: -D: Output file address for state-action pair
[9]: -L: Output file address for state label
*********************************************************
```

## Examples

1. ./run rddl.sim.Simulator -R files/Reservoir/Reservoir_det.rddl -P rddl.policy.domain.reservoir.StochasticReservoirPolicy -I is1 -V rddl.viz.GenericScreenDisplay

2. ./run rddl.sim.DomainExplorer -R files/Reservoir/Reservoir_det.rddl -P rddl.policy.domain.reservoir.StochasticReservoirPolicy -I is1 -V rddl.viz.ValueVectorDisplay

# Added Functions

1. State.getPossibleTerms(...): Used to find most possible terms given partial fluents known or true value known.
2. Help class: Used to store all command helping information. This will be extended to give instruction for public interfaces later.
