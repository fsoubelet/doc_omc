# Loading a model from into Kmod GUI

You can load the model created from the [Beta-Beat GUI](../betabeat/gui.md) or [Multiturn GUI](../multiturn/gui.md) for each beam by pressing the `load model` button.
Select the desired model directory in the pop-up dialog and confirm by pressing the `open` button.
If everything worked fine and the specified folder contains the needed `twiss_elements` file, the GUI will display the model's name.

You can choose another model directory by pressing on the `update model` button which appears if a model is already selected.
The model data is used for preset values in the GUI and the orbit-offset script needs the model for its calculations.

<figure>
  <img src="../../assets/images/kmod_gui/load_model.png" width="100%" />
  <figcaption>Loading a Model</figcaption>
</figure>


??? tip "Setting the Beta-Beat.src directory"

    To change the setting of the used `Beta-Beat.src` directory, navigate to `File` -> `Set Beta-Beat dir` and select the location where the `Beta-Beat.src` directory to be used is located.
    The Kmod GUI will automatically take the proper Python scripts from this directory.
    This is automatically reset to the standard directory `/afs/cern.ch/eng/sl/lintrack/Beta-Beat.src/`.
    
    The GUI will check if the `Beta-Beat.src` directory contains the `ProgramVersions.properties` file, which is needed for calling an external python script.
    You can change the standard directory by creating a `user.properties` file in the project folder.
    The kmod GUI will automatically read this file and change the Beta-Beat.src directory to this new value.
    This file must contain `BetaBeatDir=[newBBdir]` (replace the placeholder correctly).