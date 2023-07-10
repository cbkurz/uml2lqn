# UML2LQN

## Context
This work realizes transformations from UML diagrams to Layered Queuing Networks (LQN).
The transformations are created with the Epsilon Transformation Language (ETL).
The ETL is a model-to-model transformation language that transforms models defined in Ecore.

The main file where the transformation takes place is the `uml2lqn.etl`.
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
