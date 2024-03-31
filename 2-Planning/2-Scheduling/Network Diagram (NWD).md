Map of the sequence of activities.

Example:
![[Network Diagram_example.png]]

## Relationships

![[NetworkDiagram_relationships.png]]

![[NetworkDiagram_dependencyRelationships.png]]

Find the relationship between activities:
- Which activities must be completed immediately before this activity? (predecessor activities)
- Which activities must immediately follow this activity (successor activities)
- Which activities can occur while this activity is taking place? (parallel or concurrent activities/relationships)

![[NetworkDiagram_sequenceOfActivities.png]]

## Basic Rules to Follow in Developing Project Networks
The following eight rules apply in general when developing a project network:
1. Networks flow typically from left to right.
2. An activity cannot begin until all preceding connected activities have been completed.
3. Arrows on networks indicate precedence and flow. Arrows can cross over each other.
4. Each activity should have a unique identification number.
5. An activity identification number must be larger than that of any activities that precede it.
6. Looping is not allowed (in other words, recycling through a set of activities cannot take place).
7. Conditional statements are not allowed (that is, this type of statement should not appear: if successful, do something; if not, do nothing).
8. Experience suggests that when there are multiple starts, a common start node can be used to indicate a clear project beginning on the network. Similarly, a single project end node can be used to indicate a clear ending.

## Network Computation Process

**Legend:**

| **ES** | **ID**  | **EF** |
| ------ | ------- | ------ |
| **SL** | **DES** |        |
| **LS** | **DUR** | **LF** |
- ES: Early start
- ID: Task identifier, unique ID
- EF: Early finish
- SL: Slack. How much we can postpone the start and still not delay the project (SL = LS - ES)
- LS: Late start
- DUR: Duration of task (in calendar time units)
- LF: Late finish

### Forward Pass
- When can an activity start? (Early start, ES)
- How soon can it finish? (Early finish, EF)
- How soon can the project be finished? (expected time, TE)

1. Go from left to right and calculate ES and EF
	1. ES = highest EF of preceding activities 
	2. EF = ES + DUR
2. TE is the EF of the last activity


![[NetworkDiagram_forwardpass.png]]
### Backward Pass
- How late can an activity start? (Late Start – LS)
- How late can an activity finish? (Late finish – LF)
- Which activities represent the Critical Path (CP)? This is the longest path in the network which, when delayed, will delay the project (the path with no slack)
- How long can an activity be delayed? (slack or float, SL)

1. Go from right to left and calculate LS and LF
	1. LF = highest LS of successor activities
	2. LS = LF - DUR
2. Calculate Slack
	1. SL = LS - ES (or LF - EF)
3. Identify the Critical Path (CP): "the longest sequence of activity on a project that carry zero free slack"

![[NetworkDiagram_backwardsPass.png]]


