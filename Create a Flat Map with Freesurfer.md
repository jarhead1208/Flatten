# Set Up Freesurfer7 
Set up the home directory and configure Freesurfer7.
```
export FREESURFER_HOME=~/freesurfer7
source $FREEUSRFER_HOME/SetUpFreeSurfer.sh
```

# Read and Cut the Surface
Read the left hemisphere in Freesurfer7
```
tksurferfv  $Subject_id lh inflated
```
Cut the inflated surface like this.
![Cut](https://imgbb.com/QMYyDxB)
Save it as a patch as `lh.full.patch.3d`.
# Set Up Freesurfer6
Set up the home directory and configure Freesurfer6.
```
export FREESURFER_HOME=~/freesurfer6
source $FREEUSRFER_HOME/SetUpFreeSurfer.sh
```
# Flatten the Saved Patch
After setting up Freesurfer6, using `mris_flatten` to flatten the saved patch.
```
mris_flatten -w 10 lh.full.patch.3d lh.full.flat.patch.3d
```
`-w 10` indicates that the program will output a patch every 10 iterations to check the progress of the program.



