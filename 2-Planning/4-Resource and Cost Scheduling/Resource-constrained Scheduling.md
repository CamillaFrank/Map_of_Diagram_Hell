Used for [[Resource-constrained Project]]s
Prioritize and allocate resources to minimize project delay without exceeding the resource limit or altering the technical network relationships.

Activities are scheduled using heuristics(rules of thumb) by following the priority rules:
1. Minimum slack
2. Smallest (least) duration
3. Lowest activity identification number

Challenges:
- Reduces slack; reduce flexibility
- Increases the number of critical and near-critical activities
- Increases scheduling complexity because resource constraints are added to technical constraints
- May make the traditional critical path no longer meaningful
- Can break the sequence and leave the network with a set of disjointed critical activities
- May cause parallel activities to become sequential
- Can change activities from critical to non-critical

**The Parallel Method**
- The parallel method is an iterative process that starts from the beginning of project time and, when the resources needed exceed the resources available, retains activities first by the priority rules

### Example

Before:
![[Resource-ConstrainedScheduling_ExampleBefore.png]]

After:
![[Resource-ConstrainedScheduling_ExampleAfter.png]]