# Development Information

This section will comprise information on how to use the repository in your work. 
This includes how to set up a working environment and what branches exist. 
It is strongly advised to watch the seminar of Dimitris Kolovos, referenced in [Epsilon](Epsilon.md).

## Setup Environment
Epsilon is integrated into Eclipse. 
Therefore, this tutorial describes how to set up the respective Eclipse environment, the required plugins, and how to run the project in Eclipse.

* Clone the project from github.
* Checkout the branch `support-workflow`
* Install the LQN-Solver by installing the project https://github.com/layeredqueuing/V5
* Download and install Eclipse Epsilon as described here: https://eclipse.dev/epsilon/download/
  * Please make sure to use Java 11 when installing

<img src="InstallEpsilon.png" alt="InstallEpsilon" width="250"/>  

* Import the project using `File > Import... > General > Existing Project into Workspace` and then choose the location of the git repository.
* Open the folder `lqnxsd` right-click on `lqn.ecore` and select `Register EPackages`\

<img src="RegisterEPackages.png" alt="RegisterEPackages" width="250"/>

* For the run to work, there are more packages required. Go to `Help` > `Install New Software...` and install the following packages in the given order:
  * https://download.eclipse.org/releases/luna/ (only the `Modelling` bullet point is required)
  * http://download.eclipse.org/modeling/mdt/papyrus/updates/releases/neon
  * http://dice-project.github.io/DICE-Profiles/updates
* Right-click on the `launch.xml` (the ANT file that executes the workflow), choose `Run As > Ant Build ... ` and the ANT configuration Dialog will open. 
  * Select the `BackAnnotation` target instead of `LoadModels` 
  * Go to the `JRE` tab and configure the JRE to use the `Run in the same JRE as the workspace`
  * The `launch.xml` has three variables, `input` `name` and `output`. Provide them by opening the `Main` tab and entering them in the textarea `Arguments` `-Dinput=models -Dname=sample -Doutput=output`
  * Click on `Run`
  * If everything works correctly, the Build will execute successfully.
<img src="AntConfigurationDialog.png" alt="AntConfigurationDialog" height="300"/>
* If you want to use the workflow, you can provide your own UML diagrams to solve them by calling the launch.xml from another ANT script which provides the parameters `input`, `name` and `output`.

## Branches
This section will give a short overview of the branches that are present in this repository and their purpose.

### Master
TODO


### Support-Workflow
In this branch, the workflow to execute the UML to LQN lives.
The workflow is present in the `launch.xml`, and the LQN Ecore definition is also here.

### Easier
TODO
