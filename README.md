# UML2LQN

## Context
In this work transformations from UML diagrams to Layered Queuing Networks (LQN) are realized.
The transformations are created with the Epsilon Transformation Language (ETL).
The ETL is a model to model transformation language that allows to transform models which are defined in Ecore.

The main file where the transformation takes place is the uml2lqn.etl.
The mapping done from UML to LQN in the transformation is the following:

| UML		| LQN       |
| --------- | --------- |
| Model		| Schema    |
| Node		| Processor |
| Actor		| Task      |
| Component | Task      |
| BES       | Entry     |
| Message   | Activity  |


# Layout
* [Epsilon](documentation/Epsilon.md)
* [Related Work](documentation/RelatedWork.md)
* [Developer Information](documentation/DeveloperInformation.md)
